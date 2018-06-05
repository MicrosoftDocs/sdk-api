---
UID: NF:winsync.ICoreFragment.GetColumnCount
title: ICoreFragment::GetColumnCount
author: windows-sdk-content
description: Gets the number of columns that are contained in this knowledge fragment.
old-location: winsync\icorefragment_getcolumncount.htm
old-project: winsync
ms.assetid: 5f1aff6d-4fdf-48e1-9c7b-c003ec27f354
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetColumnCount, GetColumnCount method [Windows Sync], GetColumnCount method [Windows Sync],ICoreFragment interface, ICoreFragment interface [Windows Sync],GetColumnCount method, ICoreFragment.GetColumnCount, ICoreFragment::GetColumnCount, winsync.icorefragment_getcolumncount, winsync/ICoreFragment::GetColumnCount
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ICoreFragment.GetColumnCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ICoreFragment::GetColumnCount


## -description


Gets the number of columns that are contained in this knowledge fragment.


## -parameters




### -param pColumnCount [out]

Returns the number of columns that are contained in this knowledge fragment.


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
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -remarks



An <b>ISyncKnowledge2</b> object contains one or more <b>ICoreFragment</b> objects. Each object contains knowledge that applies to a specific set of columns. A column is represented as a change unit. Typically, one of the <b>ICoreFragment</b> objects contains no columns. When an <b>ICoreFragment</b> object contains no columns, its knowledge applies to all of the change units that are not specified in any other fragment.




## -see-also




<a href="https://msdn.microsoft.com/3e232531-ad44-4ad1-b186-46edbc07291b">ICoreFragment Interface</a>
 

 

