---
UID: NF:winsync.ISyncKnowledge.GetSingleItemExceptions
title: ISyncKnowledge::GetSingleItemExceptions
author: windows-sdk-content
description: Gets an object that can enumerate the ISingleItemException objects that are stored in the knowledge.
old-location: winsync\isyncknowledge_getsingleitemexceptions.htm
old-project: winsync
ms.assetid: d224d2b8-343d-48f9-ac87-cd6e8682987a
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSingleItemExceptions, GetSingleItemExceptions method [Windows Sync], GetSingleItemExceptions method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetSingleItemExceptions method, ISyncKnowledge.GetSingleItemExceptions, ISyncKnowledge::GetSingleItemExceptions, winsync.isyncknowledge_getsingleitemexceptions, winsync/ISyncKnowledge::GetSingleItemExceptions
ms.prod: windows
ms.technology: windows-sdk
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
 - ISyncKnowledge.GetSingleItemExceptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge::GetSingleItemExceptions


## -description


Gets an object that can enumerate the <b>ISingleItemException</b> objects that are stored in the knowledge.


## -parameters




### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumSingleItemExceptions</b>.


### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that can enumerate the list of <b>ISingleItemException</b> objects that is contained in the knowledge.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from <b>GetSingleItemExceptions</b>.




## -see-also




<a href="https://msdn.microsoft.com/623553cb-9dc2-4504-9c49-357a0526b130">ISingleItemException Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

