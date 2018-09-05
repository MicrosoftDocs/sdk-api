---
UID: NN:winsync.ISingleItemException
title: ISingleItemException
author: windows-sdk-content
description: Represents an item to exclude from a knowledge object.
old-location: winsync\isingleitemexception.htm
old-project: winsync
ms.assetid: 623553cb-9dc2-4504-9c49-357a0526b130
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISingleItemException, ISingleItemException interface [Windows Sync], ISingleItemException interface [Windows Sync],described, winsync.isingleitemexception, winsync/ISingleItemException
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISingleItemException
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISingleItemException interface


## -description


Represents an item to exclude from a knowledge object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISingleItemException</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISingleItemException</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISingleItemException</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e212e561-9baa-46d0-90c0-ec143b24e641">GetClockVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with the item exception.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bcea395-d383-434f-b3a6-cffd4419fce3">GetItemId</a>
</td>
<td align="left" width="63%">
Gets the ID of the item that is specified in the exception.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

