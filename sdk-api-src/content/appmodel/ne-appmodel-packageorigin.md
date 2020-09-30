---
UID: NE:appmodel.PackageOrigin
title: PackageOrigin (appmodel.h)
description: Specifies the origin of a package.
helpviewer_keywords: ["PackageOrigin","PackageOrigin enumeration [App packaging and management]","PackageOrigin_DeveloperSigned","PackageOrigin_DeveloperUnsigned","PackageOrigin_Inbox","PackageOrigin_LineOfBusiness","PackageOrigin_Store","PackageOrigin_Unknown","PackageOrigin_Unsigned","appmodel/PackageOrigin","appmodel/PackageOrigin_DeveloperSigned","appmodel/PackageOrigin_DeveloperUnsigned","appmodel/PackageOrigin_Inbox","appmodel/PackageOrigin_LineOfBusiness","appmodel/PackageOrigin_Store","appmodel/PackageOrigin_Unknown","appmodel/PackageOrigin_Unsigned","appxpkg.packageorigin"]
old-location: appxpkg\packageorigin.htm
tech.root: appxpkg
ms.assetid: 0CB9CE97-8A54-4BE7-B054-00F29D36CAB2
ms.date: 12/05/2018
ms.keywords: PackageOrigin, PackageOrigin enumeration [App packaging and management], PackageOrigin_DeveloperSigned, PackageOrigin_DeveloperUnsigned, PackageOrigin_Inbox, PackageOrigin_LineOfBusiness, PackageOrigin_Store, PackageOrigin_Unknown, PackageOrigin_Unsigned, appmodel/PackageOrigin, appmodel/PackageOrigin_DeveloperSigned, appmodel/PackageOrigin_DeveloperUnsigned, appmodel/PackageOrigin_Inbox, appmodel/PackageOrigin_LineOfBusiness, appmodel/PackageOrigin_Store, appmodel/PackageOrigin_Unknown, appmodel/PackageOrigin_Unsigned, appxpkg.packageorigin
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
targetos: Windows
req.typenames: PackageOrigin
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PackageOrigin
 - appmodel/PackageOrigin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppModel.h
api_name:
 - PackageOrigin
---

# PackageOrigin enumeration


## -description

Specifies the origin of a package.

## -enum-fields

### -field PackageOrigin_Unknown

The package's origin is unknown.

### -field PackageOrigin_Unsigned

The package originated as unsigned.

### -field PackageOrigin_Inbox

The package was included inbox.

### -field PackageOrigin_Store

The package originated from the Windows Store.

### -field PackageOrigin_DeveloperUnsigned

The package originated as developer unsigned.

### -field PackageOrigin_DeveloperSigned

The package originated as developer signed.

### -field PackageOrigin_LineOfBusiness

The package originated as a line-of-business app.

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-getstagedpackageorigin">GetStagedPackageOrigin</a>