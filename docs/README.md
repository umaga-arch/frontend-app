const path = require('path');
const fs = require('fs');

const packageJson = JSON.parse(fs.readFileSync(path.join(__dirname, 'package.json'), 'utf8'));

const dependencies = packageJson.dependencies;

console.log(`# frontend-app dependencies`);

for (const [name, version] of Object.entries(dependencies)) {
  console.log(`* ${name}@${version}`);
}