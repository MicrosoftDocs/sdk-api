---
UID: NF:ocidl.IPropertyPageSite.GetLocaleID
title: IPropertyPageSite::GetLocaleID
author: windows-sdk-content
description: Retrieves the locale identifier (an LCID) that a property page can use to adjust its locale-specific settings.
old-location: com\ipropertypagesite_getlocaleid.htm
tech.root: com
ms.assetid: d569346d-4a40-42a4-ac8e-539588c4dd66
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetLocaleID, GetLocaleID method [COM], GetLocaleID method [COM],IPropertyPageSite interface, IPropertyPageSite interface [COM],GetLocaleID method, IPropertyPageSite.GetLocaleID, IPropertyPageSite::GetLocaleID, _ctrl_ipropertypagesite_getlocaleid, com.ipropertypagesite_getlocaleid, ocidl/IPropertyPageSite::GetLocaleID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPageSite.GetLocaleID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- ocidl.h
: 
- IPropertyPageSite.GetLocaleID
: 
---

# IPropertyPageSite::GetLocaleID


## -description


Retrieves the locale identifier (an LCID) that a property page can use to adjust its locale-specific settings.


## -parameters




### -param pLocaleID [out]

A pointer to a variable that receives the locale identifier. See <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">Language Identifier Constants and Strings</a>.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pLocaleID</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a>



<a href="https://msdn.microsoft.com/d65d8239-495c-4eee-bd9c-8e803fd09a06">OCPFIPARAMS</a>



<a href="https://msdn.microsoft.com/363fd45f-fb36-41f0-9d72-dc9c018859ec">PROPPAGEINFO</a>
 

 

