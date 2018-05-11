---
UID: NS:textstor.TS_STATUS
title: TS_STATUS
author: windows-driver-content
description: The TS_STATUS structure contains document status data.
old-location: tsf\ts_status.htm
old-project: TSF
ms.assetid: d27d81f2-8599-4b65-866b-4e8fd2f589f5
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: TS_STATUS, TS_STATUS structure [Text Services Framework], _tsf_ts_status_ref, textstor/TS_STATUS, tsf.ts_status
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TS_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Textstor.h
api_name:
-	TS_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TS_STATUS structure


## -description



The <b>TS_STATUS</b> structure contains document status data.




## -struct-fields




### -field dwDynamicFlags

Contains a set of flags that can be changed by an app at run time. For example, an app can enable a check box for the user to reset the document status. This member can contain zero, or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TS_SD_LOADING</td>
<td>The document is loading.</td>
</tr>
<tr>
<td>TS_SD_READONLY</td>
<td>The document is read-only.</td>
</tr>
</table>
 


### -field dwStaticFlags

Contains a set of flags that cannot be changed at run time. This member can contain zero, or one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TS_SS_DISJOINTSEL</td>
<td>The document supports multiple selections.</td>
</tr>
<tr>
<td>TS_SS_REGIONS</td>
<td>The document can contain multiple regions.</td>
</tr>
<tr>
<td>TS_SS_TRANSITORY</td>
<td>The document is expected to have a short usage cycle.</td>
</tr>
<tr>
<td>TS_SS_NOHIDDENTEXT</td>
<td>The document will never contain hidden text.</td>
</tr>
<tr>
<td>TS_SS_TKBAUTOCORRECTENABLE</td>
<td><b>Starting with Windows 8:</b> The document supports autocorrection provided by the touch keyboard.</td>
</tr>
<tr>
<td>TS_SS_TKBPREDICTIONENABLE</td>
<td><b>Starting with Windows 8:</b> The document supports text suggestions provided by the touch keyboard.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/6ed040ac-8584-4f09-9af8-218b5cd33765">ITextStoreACP::GetStatus
      </a>



<a href="https://msdn.microsoft.com/44ecc116-e6f3-48dd-9bff-16d3c1e4cc97">
        ITextStoreACPSink::OnStatusChange
      </a>



<a href="https://msdn.microsoft.com/61192268-5a5f-4caa-bdb8-799ee4aea24e">
        ITextStoreAnchor::GetStatus
      </a>



<a href="https://msdn.microsoft.com/28bdfa93-29c1-4a9f-b85e-20c39a1b429b">
        ITextStoreAnchorSink::OnStatusChange
      </a>
 

 

