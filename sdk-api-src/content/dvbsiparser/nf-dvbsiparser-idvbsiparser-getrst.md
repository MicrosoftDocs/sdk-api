---
UID: NF:dvbsiparser.IDvbSiParser.GetRST
title: IDvbSiParser::GetRST
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsiparser_getrst.htm
tech.root: MSTV
ms.assetid: 263abb39-3f8d-4501-985c-d5ac9b1c9ea1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRST, GetRST method [Microsoft TV Technologies], GetRST method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetRST method, IDvbSiParser.GetRST, IDvbSiParser::GetRST, IDvbSiParserGetRST, dvbsiparser/IDvbSiParser::GetRST, mstv.idvbsiparser_getrst
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - dvbsiparser.h
api_name:
 - IDvbSiParser.GetRST
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSiParser::GetRST


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRST</b> method retrieves the running status table (RST).


## -parameters




### -param dwTimeout [in]

Specifies a time-out value, in milliseconds. If the filter does not receive the data within the time-out period, the method fails.


### -param ppRST [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/deee44cb-92b8-4d10-91d7-c99324ab5832">IDVB_RST</a> interface pointer. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive the table in the allotted time.

</td>
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




<a href="https://msdn.microsoft.com/092162af-5f88-4ce5-ac2f-89327f094804">IDvbSiParser Interface</a>
 

 

