# Micro-Credential Meta-data Standard draft

Based on the Qualifications metadata schema and ESCO data schema, extended with MicroHE: http://helium.ijs.si/microhe/escomc.html

The schema defines the following properties:

## 1. INFORMATION IDENTIFYING THE AWARDING BODY 

### `Owner` (URI: dcterms:rightsHolder)

Defined by `Owner` property.

Usage Note: Refers to the owner of the qualification. The organization owning rights over the qualification. For example, an awarding body, a national or regional authority or an international organization.

### `Provenance Agent` (URI: dcterms:creator)

Defined by `Provenance Agent` property.

Usage Note: Organisation primarily responsible for establishing defining and managing the qualification and its curricula. Sub-creator can be a natural person

### `Public key` (URI: microhe:PublicKey)

Defined by `Public key` property.

Usage Note: Public Key the institution uses to identify itself and authenticate the credentials.

### `Accreditation` (URI: esco:hasAccreditation)

Defined by `Accreditation` property.

Usage Note: Information related to the accreditation, quality assurance and regulation of a qualification, such as the agent that was primarily responsible for the accreditation, the date the accreditation was formally approved, the review- and/or expiry date and additional information about the accreditation and used standards in the assessment and quality assurance of the qualification. 

### `Homepage` (URI: foaf:homepage)

Defined by `Homepage` property.

Usage Note: The homepage (a public web document) of a qualification. There can be only one qualification that has a particular homepage.

## 2. INFORMATION IDENTIFYING THE EDUCATIONAL CREDENTIAL 

### `Identifier` (required, URI: adms:identifier)

Defined by `Identifier` property.

Usage Note: This property refers to an (alternative) identifier of a qualification like a national code or any other unique code issued by some agency and/or system. This can be on any level: an international, national, regional, private or institutional level (e.g. the unique and persistent identifier of the qualification within the publishing system). 
(See Identifying Resources and How to work with Identifiers?)

### `Title` (required, URI: skos:prefLabel)

Defined by `recipient` property.

Usage Note: The exact and official title of the qualification, in a given language. This property can be repeated for parallel language versions of the title. There can be no more than one title per language. It is mandatory to mention the title at least in the reference language if specified. See Multilingual Aspects for more information..

### `Alternative label` (URI: skos:altLabel)

Defined by `Alternative label` property.

Usage Note: An alternative name of the qualification (e.g. synonym, acronym).

### `Definition` (URI: skos:definition)

Defined by `Definition` property.

Usage Note: Short and abstract description about the qualification. This property contains a free-text and can be repeated for parallel language versions of the definition. There can be no more than one definition per language. It is mandatory to mention the definition at least in the reference language if specified. See NodeLiteral and How to work with NodeLiterals?

### `Learning outcome description` (URI: dcterms:description)

Defined by `Learning outcome description` property - The full learning outcome description of the qualification. 

Usage Note: This property contains a free-text and can be repeated for parallel language versions of the learning outcome description. There can be no more than one learning outcome description per language. It is mandatory to mention the description at least in the reference language if specified. See NodeLiteral and How to work with NodeLiterals?

### `Field` (regured, URI: esco:hasISCED-FCode)

Defined by `Field` property.

Usage note: This property relates the qualification to the ISCED. FoET 2013 classification code (Field of Education and Training Code). It indicates the thematic area of the qualification. See Controlled vocabularies to be used.

### `EQF level` (URI: esco:hasAssociation, required, (non-applicable for qualifications which are not part of national qualifica- tions framework))

Defined by `EQF level` property.

Usage Note: This property relates the qualification to the level as specified by the European Qualification Framework. See AssociationObject.

### `NQF Level` (URI: esco:hasAssociation)

Defined by `NQF Level` property.

Usage Note: This property relates the qualification to the National or Regional Qualification Framework level. See AssociationObject.

### `Number of Credit Points` (URI: microhe:hasCreditPoints)

Defined by `Number of Credit Points` property.

Usage Note: This property contains the credit points assigned to the qualification, following the credit system outlined above.

### `ECTS credit points` (URI: esco:hasECTSCreditPoints)

Defined by `ECTS credit points` property.

Usage Note: This property contains the credit points assigned to the qualification, following in the ECTS credit system.

### `Volume of learning` (URI: esco:volumeOfLearning)

Defined by `Volume of learning` property.

Usage Note: This property contains an indication of how many hours of learning efforts are needed, i.e. notional learning hours.

### `Is partial qualification` (URI: esco:isPartialQualification)

Defined by `Is partial qualification` property.

Usage Note: Indicates whether a qualification is a full qualification or part of another qualification. In the latter, the qualification is only obtained as a formal outcome of a “broader” qualification of which it is part. 
The default value is ‘false’.

### `Ways to acquire` (URI: esco:waysToAcquire )

Defined by `Ways to acquire` property.

Usage Note: This property indicates whether the qualification can be acquired by validation of a formal, non-formal and/or informal learning processes. 
The different ways are encoded as skos:Concepts in a controlled vocabulary defined by the QMS (see Controlled vocabularies to be used).

### `Educational Credential Type` (URI: microhe:hasAssociation linked to microhe:CreditSystem)

Defined by `Educational Credential Type` property.

Usage Note: Provide the full name of the qualification type or credit system in use, such as ECTS, degrees etc.

### `Entry requirement` (URI: esco:hasEntryRequirement)

Defined by `Entry requirement` property.

Usage Note: This property refers to an entry requirement of the qualification.

### `Expiry period` (URI: esco:expiryPeriod)

Defined by `Expiry period` property.

Usage Note: The validity period of a qualification.  

### `Learning outcome` (URI: esco:hasAssociation)

Defined by `Learning outcome` property.

Usage Note: Expresses a learning outcome of the qualification as a relation to a skill, competence or knowledge from a known framework or standard classification. The recommended framework is ESCO. See AssociationObject 
Minimum 1 of each skill, competence, knowledge.

### `Related occupation` (URI: esco:hasAssociation)

Defined by `Related occupation` property.

Usage Note: Relates the qualification to an occupation or occupational field from a known framework or standard classification. The recommended framework is ESCO. See AssociationObject.

### `Recognition` (URI: esco:hasRecognition)

Defined by `Recognition` property.

Usage Note: Information related to the formal recognition of a qualification, such as the country and/or region where the qualification was recognised and optionally the date of formal recognition.

### `Awarding body` (URI: microhe:AwardingBody)

Defined by `Awarding body` property.

### `Awarding activity (Required to specify the awarding body/ compe- tent authority and the Country/Region)` (URI: esco:hasAssociation)

Defined by `Awarding activity` property.

Usage Note: Refers to an activity related to the awarding of the qualification, such as the country or region where the qualification is awarded, the awarding body and optionally the awarding period.

### `Awarding method` (URI: microhe:AwardingMethod)

Defined by `Awarding method` property.

Usage Note: Is the qualification certified through:
•	undergoing the learning activity
•	an assessment of competence acquired

### `Grade scheme` (URI: microhe:GradeScheme)

Defined by `Grade scheme` property.

Usage Note: Description of  the grading scheme, and what the grade means.

### `Mode of Study` (URI: microhe:mode)

Defined by `Mode of Study` property.

Usage Note: Online / Face to Face / Practice / Workplace / informal learning.

### `Assessment method` (URI: microhe:Assessmentmethod)

Defined by `Assessment method` property.

Usage Note: Description of the form of assessment.

### `Landing page` (URI: dcat:landingPage)

Defined by `Landing page` property.

Usage Note: A web page that can be navigated to in a web browser to gain access to the qualification and/or additional information. A qualification might not have a homepage but instead a landing page.

### `Supplementary document` (URI: esco:supplementaryDoc)

Defined by `Supplementary document` property.

Usage Note: A public web document containing additional documentation about the qualification, such as a diploma or certificate supplement. It can be any document containing further information about the qualification. The document can be a web page that can be navigated or a downloadable file.
See Document and How to work with Documents?

## 3. INFORMATION IDENTIFYING THE CREDENTIAL TYPE 

### `Credit / Token System` (URI: microhe:CreditSystem)

Defined by `Credit / Token System` property.

Usage Note: Name of the Credit system in use, such as ECTS etc. Relational to microHE:CreditSystem_type

### `Credit System Title` ((URI: microhe:CreditSystem_label)

Defined by `Credit System Title` property.

Usage Note: The exact and official title of the credential-type/credit-system if available.

### `Credit System Definition` (URI: microhe:CreditSystem_definition)

Defined by `Credit System Definition` property.

Usage Note: Short and abstract description about the credential type/credential system

### `Credit System Value` (URI: microhe:CreditSytem_value)

Defined by `Credit System Value` property.

Usage Note: Value described in terms of hours, certificates, accomplishments or other measure used for the token

### `Credit System Issuer` (URI: dcterms:creator)

Defined by `Credit System Issuer` property.

Usage Note: Which organization / consortium / law regulates who can issue this token.

### `Can consist of` (URI: microhe:hasAssociation)

Defined by `Can consist of` property.

Usage Note: Which other credential type/credit system can be used to build this credential type/credit system.

### `Credit System Reference Number` (URI: adms:identifier)

Defined by `Credit System Reference Number` property.

Usage Note: Reference number.

### `Reference language (URI: esco:referenceLanguage)

Defined by `Reference language property.

Usage Note: The ISO 639-1 code of the language (2-char language code) in which information about the qualification is published. This language will be used as the default reference language for the qualification.

## 4. INFORMATION IDENTIFYING THE HOLDER OF THE EDUCATIONAL CREDENTIAL AND THEIR ACCOMPLISHMENT 

### `Is made up of` (URI: microhe:consistsof)

Defined by `Is made up of` property.

Usage Note: Describes the (micro) qualifications which have been linked together to create the qualification.

### `Expiry period` (URI: esco:expiryPeriod)

Defined by `Expiry period` property.

Usage Note: The validity period of a qualification.

### `Holder's Name` (URI: microhe:Holder)

Defined by `Holder's Name` property.

Usage Note: Name of the person receiving the credential.

### `Date of birth` (URI:)

Defined by `Date of birth` property.

Usage Note: Date of birth of the person receiving the credential in day/month/year in format

### `Student ID` (URI: microhe:PublicKey)

Defined by `Student ID` property.

Usage Note: Student identification number or code or public key used to authenticate student.

### `Grade` (URI: microhe:Grade)

Defined by `Grade` property.

Usage Note: Grade achieved.

### `Credits awarded` (URI: microhe:hasCreditPoints)

Defined by `Credits awarded` property.

Usage Note: Number of credits awarded.

### `Sub-Credentials contained` (URI: microhe:consistsOf)

Defined by `Sub-Credentials contained` property.

Usage Note: Other credentials which may make up this credential, by Unique Identifer.

### `Unique Identifier` (URI: adms:identifier)

Defined by `Unique Identifier` property.

Usage Note: Automatically generated for each credential

### `Supplementary evidence` (URI: esco:supplementaryDoc)

Defined by `Supplementary evidence` property.

Usage Note: A public web document containing additional documentation about the credential awarded to the user, such as a diploma or certificate supplement, or a doctoral dissertation.

### `Credential` (URI: aicrohe:hasAssociation)

Defined by `Credential` property.

Usage Note: The credential which is being awarded to the student.

### `Expiry Period` (URI: esco:expiryPeriod)

Defined by `Expiry Period` property.

Usage Note: Date on which the credential will expire.

## Additional Fields

### `Release/publication date` (URI: dcterms:issued)

Defined by `Release/publication date` property.

Usage Note: Date of formal publication. The date the qualification was published and the metadata about the qualification was made available.

### `Update/modification date` (URI: dcterms:modified)

Defined by `Update/modification date` property.

Usage Note: Date when the qualification was last updated since it was published.

### `Change note` (URI: skos:changeNote)

Defined by `Change note` property.

Usage Note: A property to record information about fine grained changes of the qualification. This property contains a free-text and can be repeated for parallel language versions of the change note. See NodeLiteral and How to work with NodeLiterals?  

### `History note` (URI: skos:historyNote )

Defined by `History note` property.

Usage Note: A property to record information about major lifecycle changes of the qualification (e.g. past state/use/meaning of a qualification). This property contains a free-text and can be repeated for parallel language versions of the history note. See NodeLiteral and How to work with NodeLiterals?

### `Additional note` (URI: esco:additionalNote)

Defined by `Additional note` property.

Usage Note: A property to record any further information about a qualification. This property contains a free-text and can be repeated for parallel language versions of the additional note. See NodeLiteral and How to work with NodeLiterals?

### `Status` (Status (required if not valid), URI: iso-thes:status)

Defined by `Status` property.

Usage Note: The publication status of a qualification, e.g. released, obsolete, ... It MUST take one of the predefined values as specified in the section Controlled vocabularies to be used.

### `Replaces` (URI: dcterms:replaces)

Defined by `Replaces` property.

Usage Note: A related qualification that was replaced, displaced or superseded by this qualification. The learning outcomes of a qualification might change overtime and therefore result in another qualification replacing the old one

### `Replaced by` (URI: dcterms:isReplacedBy)

Defined by `Replaced by` property.

Usage Note: In case a qualification is deprecated, this property refers to the qualification that replaces, displaces or supersedes the first qualification.

### `Publisher` (URI: dcterms:publisher)

Defined by `Publisher` property.

Usage Note: Refers to the agent responsible for making the information about the qualification available.
