---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# APPX_PACKAGE_SETTINGS structure


## -description


Represents package settings used to create a package.


## -struct-fields




### -field forceZip32

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the package is created as Zip32; <b>FALSE</b> if the package is created as Zip64. The default is Zip64.


### -field hashMethod

Type: <b><b>IUri</b>*</b>

The hash algorithm URI to use for the block map of the package.


## -remarks



Set <b>forceZip32</b> to <b>TRUE</b> to maintain compatibility with older ZIP tools.

The possible values for <b>hashMethod</b> are: <ul>
<li>http://www.w3.org/2001/04/xmlenc#sha256</li>
<li>http://www.w3.org/2001/04/xmldsig-more#sha384</li>
<li>http://www.w3.org/2001/04/xmlenc#sha512</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/10E9250E-7A64-4FB0-ACB9-10CB144A0FBE">IAppxFactory::CreatePackageWriter</a>
 

 

