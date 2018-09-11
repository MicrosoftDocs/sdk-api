---
UID: NS:appmodel.PACKAGE_ID
title: PACKAGE_ID
author: windows-sdk-content
description: Represents package identification information, such as name, version, and publisher.
old-location: appxpkg\package_id.htm
tech.root: appxpkg
ms.assetid: 4B15281A-2227-47B7-A750-0A01DB8543FC
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: PACKAGE_ID, PACKAGE_ID structure [App packaging and management], appmodel/PACKAGE_IDW, appxpkg.package_id
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppModel.h
api_name:
 - PACKAGE_ID
product: Windows
targetos: Windows
req.typenames: PACKAGE_ID
req.redist: 
---

# PACKAGE_ID structure


## -description


Represents package identification information, such as name, version, and publisher.


## -struct-fields




### -field reserved

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT32</a></b>

Reserved; do not use.


### -field processorArchitecture

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT32</a></b>

The processor architecture of the package. This member must be one of the values of the <a href="https://msdn.microsoft.com/8BC7ABF0-448F-4405-AA82-49C6DB3F230C">APPX_PACKAGE_ARCHITECTURE</a> enumeration.


### -field version

Type: <b><a href="https://msdn.microsoft.com/8543DF84-A908-4DF5-AEE6-169FECB2AA97">PACKAGE_VERSION</a></b>

The version of the package.


### -field name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

The name of the package.


### -field publisher

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

The publisher of the package. If there is no publisher for the package, this member is <b>NULL</b>.


### -field resourceId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

The resource identifier (ID) of the package. If there is no resource ID for the package, this member is <b>NULL</b>.


### -field publisherId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

The publisher identifier (ID) of the package. If there is no publisher ID for the package, this member is <b>NULL</b>.


## -remarks



For info about string size limits, see <a href="https://msdn.microsoft.com/C4F81822-B502-4360-AEA4-829F1AB926BF">Identity constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/4CFC707A-2A5A-41FE-BB5F-6FECACC99271">GetCurrentPackageId</a>



<a href="https://msdn.microsoft.com/BA5D87F5-72FD-48BE-A104-EC7D1459FD58">GetPackageId</a>



<a href="https://msdn.microsoft.com/BDA0DD87-A36D-486B-BF89-EA5CC105C742">GetPackagePath</a>



<a href="https://msdn.microsoft.com/0DDE00D1-9C5F-4F2B-8110-A92B1FFA1B64">PACKAGE_INFO</a>



<a href="https://msdn.microsoft.com/198DAB6B-21D2-4ACB-87DF-B3F4EFBEE323">PackageFamilyNameFromId</a>



<a href="https://msdn.microsoft.com/0024AF55-295E-49B1-90C2-9144D336529B">PackageFullNameFromId</a>



<a href="https://msdn.microsoft.com/EED832F8-E4F7-4A0F-93E2-451F78F67767">PackageIdFromFullName</a>
 

 

