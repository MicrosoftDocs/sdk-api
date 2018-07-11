---
UID: NF:ocidl.IPropertyPageSite.TranslateAccelerator
title: IPropertyPageSite::TranslateAccelerator
author: windows-sdk-content
description: Passes a keystroke to the property frame for processing.
old-location: com\ipropertypagesite_translateaccelerator.htm
old-project: com
ms.assetid: d2233022-e66e-448c-a921-92948c05016f
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IPropertyPageSite interface [COM],TranslateAccelerator method, IPropertyPageSite.TranslateAccelerator, IPropertyPageSite::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM],IPropertyPageSite interface, _ctrl_ipropertypagesite_translateaccelerator, com.ipropertypagesite_translateaccelerator, ocidl/IPropertyPageSite::TranslateAccelerator
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPageSite.TranslateAccelerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyPageSite::TranslateAccelerator


## -description


Passes a keystroke to the property frame for processing.


## -parameters




### -param pMsg [in]

A pointer to the <a href="_win32_MSG_str_cpp">MSG</a> structure to be processed.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The page site did not process the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The page site does not support keyboard processing.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a9035a10-2078-4626-8386-f9298526dfb7">IPropertyPageSite</a>
 

 

