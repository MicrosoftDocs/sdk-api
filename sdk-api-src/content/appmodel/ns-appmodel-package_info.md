---
UID: NS:appmodel.PACKAGE_INFO
title: PACKAGE_INFO
author: windows-driver-content
description: Represents package identification information that includes the package identifier, full name, and install location.
old-location: appxpkg\package_info.htm
old-project: appxpkg
ms.assetid: 0DDE00D1-9C5F-4F2B-8110-A92B1FFA1B64
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: PACKAGE_INFO, PACKAGE_INFO structure [App packaging and management], appmodel/PACKAGE_INFO, appxpkg.package_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PACKAGE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	AppModel.h
api_name:
-	PACKAGE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PACKAGE_INFO structure


## -description


Represents package identification information that includes the package identifier, full name, and install location.


## -struct-fields




### -field reserved

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT32</a></b>

Reserved; do not use.


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT32</a></b>

Properties of the package.


### -field path

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

The location of the package.


### -field packageFullName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

The package full name.


### -field packageFamilyName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

The package family name.


### -field packageId

Type: <b><a href="https://msdn.microsoft.com/4B15281A-2227-47B7-A750-0A01DB8543FC">PACKAGE_ID</a></b>

The package identifier (ID).


## -remarks



For info about string size limits, see <a href="https://msdn.microsoft.com/C4F81822-B502-4360-AEA4-829F1AB926BF">Identity constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/A1887D61-0FAD-4BE8-850F-F104CC074798">GetCurrentPackageInfo</a>



<a href="https://msdn.microsoft.com/28F45B3B-A61F-44D3-B606-6966AD5866FA">GetPackageInfo</a>
 

 

