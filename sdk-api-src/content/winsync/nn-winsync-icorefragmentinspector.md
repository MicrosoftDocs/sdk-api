---
UID: NN:winsync.ICoreFragmentInspector
title: ICoreFragmentInspector
author: windows-sdk-content
description: Enumerates the ICoreFragment objects that are contained in a knowledge object.
old-location: winsync\icorefragmentinspector.htm
tech.root: winsync
ms.assetid: 10c22b92-bda8-42f6-9fd6-58e77e5a18d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICoreFragmentInspector, ICoreFragmentInspector interface [Windows Sync], ICoreFragmentInspector interface [Windows Sync],described, winsync.icorefragmentinspector, winsync/ICoreFragmentInspector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ICoreFragmentInspector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICoreFragmentInspector interface


## -description


Enumerates the <b>ICoreFragment</b> objects that are contained in a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICoreFragmentInspector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICoreFragmentInspector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICoreFragmentInspector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/801a2643-d954-44b8-83ce-021be893d06a">NextCoreFragments</a>
</td>
<td align="left" width="63%">
Returns the next <b>ICoreFragment</b> objects in the knowledge, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57621ce0-c484-4687-9f2f-98d285b041ca">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the knowledge.


</td>
</tr>
</table> 


## -remarks



An <b>ICoreFragmentInspector</b> object can be obtained by calling <a href="https://msdn.microsoft.com/088d864f-bb74-4fd8-b8cb-352cb2731edb">ISyncKnowledge2::GetInspector</a> on a knowledge object.




## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

