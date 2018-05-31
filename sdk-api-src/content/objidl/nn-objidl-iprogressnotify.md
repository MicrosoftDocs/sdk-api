---
UID: NN:objidl.IProgressNotify
title: IProgressNotify
author: windows-sdk-content
description: Enables applications and other objects to receive notifications of changes in the progress of a downloading operation.
old-location: com\iprogressnotify.htm
old-project: com
ms.assetid: 3f90437d-df8f-42b2-af81-519bfb9577b1
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IProgressNotify, IProgressNotify interface [COM], IProgressNotify interface [COM],described, _com_iprogressnotify, com.iprogressnotify, objidl/IProgressNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IProgressNotify
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IProgressNotify interface


## -description


Enables applications and other objects to receive notifications of changes in the progress of a downloading operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProgressNotify</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IProgressNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProgressNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07b3e629-a558-4a0e-8307-ca922f56e00c">OnProgress</a>
</td>
<td align="left" width="63%">
Notifies registered objects and applications of the progress of a downloading operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07b3e629-a558-4a0e-8307-ca922f56e00c">IProgressNotify::OnProgress</a>
 

 

