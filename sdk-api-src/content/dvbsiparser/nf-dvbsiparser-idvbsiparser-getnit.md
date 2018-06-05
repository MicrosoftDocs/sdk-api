---
UID: NF:dvbsiparser.IDvbSiParser.GetNIT
title: IDvbSiParser::GetNIT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsiparser_getnit.htm
old-project: mstv
ms.assetid: a7c802ad-908f-4778-b8db-02fff4f3a13e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetNIT, GetNIT method [Microsoft TV Technologies], GetNIT method [Microsoft TV Technologies],IDvbSiParser interface, IDvbSiParser interface [Microsoft TV Technologies],GetNIT method, IDvbSiParser.GetNIT, IDvbSiParser::GetNIT, IDvbSiParserGetNIT, dvbsiparser/IDvbSiParser::GetNIT, mstv.idvbsiparser_getnit
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbSiParser.GetNIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbSiParser::GetNIT


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetNIT</b> method retrieves the network information table (NIT).


## -parameters




### -param tableId [in]

Specifies the table identifier of the NIT. Use one of the values in the following table.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>DVB_NIT_ACTUAL_TID (0x40)</td>
<td>NIT for the network that carries this transport stream.</td>
</tr>
<tr>
<td>DVB_NIT_OTHER_TID (0x41)</td>
<td>NIT for another network.</td>
</tr>
</table>
 


### -param pwNetworkId [in]

Optional parameter that contains a network identifier. You can use this value to filter the request. Otherwise, set this parameter to <b>NULL</b>.


### -param ppNIT [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT</a> interface pointer. The caller must release the interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
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
 

 

