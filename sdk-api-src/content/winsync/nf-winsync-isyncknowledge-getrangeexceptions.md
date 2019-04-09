---
UID: NF:winsync.ISyncKnowledge.GetRangeExceptions
title: ISyncKnowledge::GetRangeExceptions (winsync.h)
author: windows-sdk-content
description: Gets an object that can enumerate the IRangeException objects that are stored in the knowledge.
old-location: winsync\isyncknowledge_getrangeexceptions.htm
tech.root: winsync
ms.assetid: 9dd945bf-a3e4-408a-bdfe-5163a7dbdc3f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRangeExceptions, GetRangeExceptions method [Windows Sync], GetRangeExceptions method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetRangeExceptions method, ISyncKnowledge.GetRangeExceptions, ISyncKnowledge::GetRangeExceptions, winsync.isyncknowledge_getrangeexceptions, winsync/ISyncKnowledge::GetRangeExceptions
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
 - ISyncKnowledge.GetRangeExceptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge::GetRangeExceptions


## -description


Gets an object that can enumerate the <b>IRangeException</b> objects that are stored in the knowledge.


## -parameters




### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumRangeExceptions</b>.


### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that can enumerate the list of <b>IRangeException</b> objects that is contained in the knowledge.


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



Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from <b>GetRangeExceptions</b>.




## -see-also




<a href="https://msdn.microsoft.com/7eea9fe0-80e7-43a9-a797-df12d4d809dc">IRangeException Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

