---
UID: NE:certenroll.ImportPFXFlags
title: ImportPFXFlags (certenroll.h)
description: Flags to use when importing a PFX certificate.helpviewer_keywords: ["ImportExportable","ImportExportableEncrypted","ImportForceOverwrite","ImportInstallCertificate","ImportInstallChain","ImportInstallChainAndRoot","ImportMachineContext","ImportNoUserProtected","ImportNone","ImportPFXFlags","ImportPFXFlags enumeration [Security]","ImportSaveProperties","ImportSilent","ImportUserProtected","ImportUserProtectedHigh","certenroll/ImportExportable","certenroll/ImportExportableEncrypted","certenroll/ImportForceOverwrite","certenroll/ImportInstallCertificate","certenroll/ImportInstallChain","certenroll/ImportInstallChainAndRoot","certenroll/ImportMachineContext","certenroll/ImportNoUserProtected","certenroll/ImportNone","certenroll/ImportPFXFlags","certenroll/ImportSaveProperties","certenroll/ImportSilent","certenroll/ImportUserProtected","certenroll/ImportUserProtectedHigh","security.importpfxflags"]
old-location: security\importpfxflags.htm
tech.root: SecCrypto
ms.assetid: B91A32A9-680F-4012-896E-7B3DF6629B25
ms.date: 12/05/2018
ms.keywords: ImportExportable, ImportExportableEncrypted, ImportForceOverwrite, ImportInstallCertificate, ImportInstallChain, ImportInstallChainAndRoot, ImportMachineContext, ImportNoUserProtected, ImportNone, ImportPFXFlags, ImportPFXFlags enumeration [Security], ImportSaveProperties, ImportSilent, ImportUserProtected, ImportUserProtectedHigh, certenroll/ImportExportable, certenroll/ImportExportableEncrypted, certenroll/ImportForceOverwrite, certenroll/ImportInstallCertificate, certenroll/ImportInstallChain, certenroll/ImportInstallChainAndRoot, certenroll/ImportMachineContext, certenroll/ImportNoUserProtected, certenroll/ImportNone, certenroll/ImportPFXFlags, certenroll/ImportSaveProperties, certenroll/ImportSilent, certenroll/ImportUserProtected, certenroll/ImportUserProtectedHigh, security.importpfxflags
f1_keywords:
- certenroll/ImportPFXFlags
dev_langs:
- c++
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- certenroll.h
api_name:
- ImportPFXFlags
targetos: Windows
req.typenames: ImportPFXFlags
req.redist: 
ms.custom: 19H1
---

# ImportPFXFlags enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Flags to use when importing a PFX certificate.


## -enum-fields




### -field ImportNone

None


### -field ImportMachineContext

Import the PFX certificate into the machine certificate store; otherwise install to the user certificate store.


### -field ImportForceOverwrite

Overwrite existing certificate, if exists.


### -field ImportSilent

Silently perform the operation (do not show a user interface).


### -field ImportSaveProperties

Save Properties on the imported PFX file.


### -field ImportExportable

Import the PFX certificate’s private key as exportable


### -field ImportExportableEncrypted

Import the PFX certificate’s private key as exportable and encrypted.


### -field ImportNoUserProtected

Import the PFX certificate’s private key to not require consent.


### -field ImportUserProtected

Import the PFX certificate’s private key to require consent without a password.


### -field ImportUserProtectedHigh

Import the PFX certificate’s private key to require consent with a password.


### -field ImportInstallCertificate

Install the PFX certificate to the certificate store.


### -field ImportInstallChain

Install the PFX certificate’s chain to the certificate store.


### -field ImportInstallChainAndRoot

Install the PFX certificate’s chain and root to the certificate store.

