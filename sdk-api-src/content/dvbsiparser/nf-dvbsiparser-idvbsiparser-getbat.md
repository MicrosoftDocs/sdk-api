---
UID: NF:dvbsiparser.IDvbSiParser.GetBAT
title: IDvbSiParser::GetBAT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsiparser_getbat.htm
tech.root: MSTV
ms.assetid: dc9cd50f-a9cc-436c-a416-9fc4de506a9e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetBAT, GetBAT method [Microsoft TV Technologies], GetBAT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetBAT method, IDvbSiParser.GetBAT, IDvbSiParser::GetBAT, IDvbSiParserGetBAT, dvbsiparser/IDvbSiParser::GetBAT, mstv.idvbsiparser_getbat
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
 - IDvbSiParser.GetBAT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSiParser::GetBAT


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetBAT</b> method retrieves the bouquet association table (BAT).


## -parameters




### -param pwBouquetId [in]

Optional parameter that contains a bouquet identifier. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.


### -param ppBAT [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/c312a152-21ee-4708-90a8-ab9bde9a2011">IDVB_BAT</a> interface pointer. The caller must release the interface.


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
<b>NULL</b> pointer argument.

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
 




## -remarks



The method fails if the filter does not receive a matching table within a predetermined length of time.




## -see-also




<a href="https://msdn.microsoft.com/092162af-5f88-4ce5-ac2f-89327f094804">IDvbSiParser Interface</a>
 

 

