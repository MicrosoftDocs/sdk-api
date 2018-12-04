---
UID: NF:textstor.ITextStoreAnchorSink.OnStatusChange
title: ITextStoreAnchorSink::OnStatusChange
author: windows-sdk-content
description: ITextStoreAnchorSink::OnStatusChange method
old-location: tsf\itextstoreanchorsink_onstatuschange.htm
tech.root: TSF
ms.assetid: 28bdfa93-29c1-4a9f-b85e-20c39a1b429b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnStatusChange method, ITextStoreAnchorSink.OnStatusChange, ITextStoreAnchorSink::OnStatusChange, OnStatusChange, OnStatusChange method [Text Services Framework], OnStatusChange method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onstatuschange_ref, textstor/ITextStoreAnchorSink::OnStatusChange, tsf.itextstoreanchorsink_onstatuschange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchorSink.OnStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchorSink::OnStatusChange


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
 




## -remarks



Applications should call this method whenever <a href="https://msdn.microsoft.com/61192268-5a5f-4caa-bdb8-799ee4aea24e">ITextStoreAnchor::GetStatus</a> returns a new value for any of the <b>dwDynamicFlags</b> member of <b>TS_STATUS</b> .




## -see-also




<a href="https://msdn.microsoft.com/61192268-5a5f-4caa-bdb8-799ee4aea24e">ITextStoreAnchor::GetStatus
      </a>



<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a>



<a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS
      </a>
 

 

