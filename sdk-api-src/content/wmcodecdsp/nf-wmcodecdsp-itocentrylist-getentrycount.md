---
UID: NF:wmcodecdsp.ITocEntryList.GetEntryCount
title: ITocEntryList::GetEntryCount
author: windows-sdk-content
description: The GetEntryCount method retrieves the number of entries in the list.
old-location: mf\itocentrylist_getentrycount.htm
old-project: medfound
ms.assetid: 74c45032-578d-4ee1-a13d-f95646f27ce9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetEntryCount, GetEntryCount method [Media Foundation], GetEntryCount method [Media Foundation],ITocEntryList interface, ITocEntryList interface [Media Foundation],GetEntryCount method, ITocEntryList.GetEntryCount, ITocEntryList::GetEntryCount, codecapi.itocentrylist_getentrycount, mf.itocentrylist_getentrycount, wmcodecdsp/ITocEntryList::GetEntryCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVideoDSPMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmvdspa.dll
api_name:
-	ITocEntryList.GetEntryCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocEntryList::GetEntryCount


## -description


The <b>GetEntryCount</b> method retrieves the number of entries in the list.


## -parameters




### -param pdwEntryCount [out]

Pointer to a <b>DWORD</b> that receives the number of entries.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cf2171c9-67ce-4acb-97cc-af17203e815b">GetEntryByIndex</a>



<a href="https://msdn.microsoft.com/98052f26-7956-4973-ab86-428e7a355937">ITocEntryList</a>
 

 

