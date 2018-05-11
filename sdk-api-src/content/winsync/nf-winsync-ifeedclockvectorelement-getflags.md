---
UID: NF:winsync.IFeedClockVectorElement.GetFlags
title: IFeedClockVectorElement::GetFlags
author: windows-driver-content
description: Gets flags that specify additional information about the clock vector element.
old-location: winsync\ifeedclockvectorelement_getflags.htm
old-project: winsync
ms.assetid: 9c618ca9-de6b-4e3e-a0cc-cac3886199d5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetFlags, GetFlags method [Windows Sync], GetFlags method [Windows Sync],IFeedClockVectorElement interface, IFeedClockVectorElement interface [Windows Sync],GetFlags method, IFeedClockVectorElement.GetFlags, IFeedClockVectorElement::GetFlags, winsync.ifeedclockvectorelement_getflags, winsync/IFeedClockVectorElement::GetFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IFeedClockVectorElement.GetFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IFeedClockVectorElement::GetFlags


## -description


Gets flags that specify additional information about the clock vector element.


## -parameters




### -param pbFlags [out]

Returns flags that specify additional information about the clock vector element. These flags will be a combination of the <b>SYNC_VERSION_FLAG</b> flags.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7ffc228f-c4f2-4451-9b23-ec78bf6c8318">IFeedClockVectorElement Interface</a>
 

 

