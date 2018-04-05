---
UID: NF:ocidl.IPropertyPageSite.TranslateAccelerator
title: IPropertyPageSite::TranslateAccelerator method
author: windows-driver-content
description: Passes a keystroke to the property frame for processing.
old-location: com\ipropertypagesite_translateaccelerator.htm
old-project: com
ms.assetid: d2233022-e66e-448c-a921-92948c05016f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IPropertyPageSite, IPropertyPageSite interface [COM], TranslateAccelerator method, IPropertyPageSite::TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM], IPropertyPageSite interface, TranslateAccelerator,IPropertyPageSite.TranslateAccelerator, _ctrl_ipropertypagesite_translateaccelerator, com.ipropertypagesite_translateaccelerator, ocidl/IPropertyPageSite::TranslateAccelerator
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPropertyPageSite.TranslateAccelerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPropertyPageSite::TranslateAccelerator method


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
 

 

