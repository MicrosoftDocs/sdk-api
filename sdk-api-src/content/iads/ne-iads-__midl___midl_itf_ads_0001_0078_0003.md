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

# __MIDL___MIDL_itf_ads_0001_0078_0003 enumeration


## -description


The <b>ADS_DISPLAY_ENUM</b> enumeration specifies how a path is to be displayed.


## -enum-fields




### -field ADS_DISPLAY_FULL

The path  is displayed with both attributes and values. For example, CN=Jeff Smith.


### -field ADS_DISPLAY_VALUE_ONLY

The path is displayed with values only. For example, Jeff Smith.


## -remarks



This enumeration is used in  <a href="https://msdn.microsoft.com/2d975482-74f6-4ffa-a243-baa5f6a8d200">IADsPathname::SetDisplayType</a> method to specify how a path  is to be displayed.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numeric constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should create explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/2d975482-74f6-4ffa-a243-baa5f6a8d200">IADsPathname::SetDisplayType</a>
 

 

