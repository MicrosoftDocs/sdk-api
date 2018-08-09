---
UID: NF:textstor.ITextStoreACPSink.OnStatusChange
title: ITextStoreACPSink::OnStatusChange
author: windows-sdk-content
description: ITextStoreACPSink::OnStatusChange method
old-location: tsf\itextstoreacpsink_onstatuschange.htm
old-project: TSF
ms.assetid: 44ecc116-e6f3-48dd-9bff-16d3c1e4cc97
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnStatusChange method, ITextStoreACPSink.OnStatusChange, ITextStoreACPSink::OnStatusChange, OnStatusChange, OnStatusChange method [Text Services Framework], OnStatusChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onstatuschange_ref, textstor/ITextStoreACPSink::OnStatusChange, tsf.itextstoreacpsink_onstatuschange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TsRunType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACPSink.OnStatusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACPSink::OnStatusChange


## -description




## -parameters




### -param dwFlags [in]

Contains a value that specifies the new status. For more information about possible values, see the <b>dwDynamicFlags</b> member of the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a>



<a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS
      </a>
 

 

