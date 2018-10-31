---
UID: NN:objidl.ICallFactory
title: ICallFactory
author: windows-sdk-content
description: Creates a call object for processing calls to the methods of an asynchronous interface.
old-location: com\icallfactory.htm
tech.root: com
ms.assetid: 323dc627-3867-4170-b278-0bce46077729
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ICallFactory, ICallFactory interface [COM], ICallFactory interface [COM],described, _com_icallfactory, com.icallfactory, objidlbase/ICallFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: ObjIdl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ICallFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallFactory interface


## -description


Creates a call object for processing calls to the methods of an asynchronous interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallFactory</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICallFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICallFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8df51aeb-4852-4dab-b1e9-e149ee115ea8">CreateCall</a>
</td>
<td align="left" width="63%">
Creates an instance of the call object that corresponds to a specified asynchronous interface.

</td>
</tr>
</table> 

