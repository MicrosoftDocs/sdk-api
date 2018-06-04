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

# ITextFont2::GetLinkType


## -description


Gets the link type.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The link type. It can be one of the following values.         


<a id="tomNoLink"></a>
<a id="tomnolink"></a>
<a id="TOMNOLINK"></a>


#### tomNoLink

<a id="tomClientLink"></a>
<a id="tomclientlink"></a>
<a id="TOMCLIENTLINK"></a>


#### tomClientLink

<a id="tomFriendlyLinkName"></a>
<a id="tomfriendlylinkname"></a>
<a id="TOMFRIENDLYLINKNAME"></a>


#### tomFriendlyLinkName

<a id="tomFriendlyLinkAddress"></a>
<a id="tomfriendlylinkaddress"></a>
<a id="TOMFRIENDLYLINKADDRESS"></a>


#### tomFriendlyLinkAddress

<a id="tomAutoLinkURL"></a>
<a id="tomautolinkurl"></a>
<a id="TOMAUTOLINKURL"></a>


#### tomAutoLinkURL

<a id="tomAutoLinkEmail"></a>
<a id="tomautolinkemail"></a>
<a id="TOMAUTOLINKEMAIL"></a>


#### tomAutoLinkEmail

<a id="tomAutoLinkPhone"></a>
<a id="tomautolinkphone"></a>
<a id="TOMAUTOLINKPHONE"></a>


#### tomAutoLinkPhone

<a id="tomAutoLinkPath"></a>
<a id="tomautolinkpath"></a>
<a id="TOMAUTOLINKPATH"></a>


#### tomAutoLinkPath


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>
 

 

