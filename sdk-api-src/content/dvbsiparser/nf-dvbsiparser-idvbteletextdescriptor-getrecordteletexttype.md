---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetRecordTeletextType
title: IDvbTeletextDescriptor::GetRecordTeletextType
author: windows-sdk-content
description: Gets the teletext type code from from a Digital Video Broadcast (DVB) teletext descriptor.
old-location: mstv\idvbteletextdescriptor_getrecordteletexttype.htm
old-project: mstv
ms.assetid: 4272d95a-406f-4afc-92b9-abfd618f41ab
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordTeletextType, GetRecordTeletextType method [Microsoft TV Technologies], GetRecordTeletextType method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetRecordTeletextType method, IDvbTeletextDescriptor.GetRecordTeletextType, IDvbTeletextDescriptor::GetRecordTeletextType, dvbsiparser/IDvbTeletextDescriptor::GetRecordTeletextType, mstv.idvbteletextdescriptor_getrecordteletexttype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
-	IDvbTeletextDescriptor.GetRecordTeletextType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbTeletextDescriptor::GetRecordTeletextType


## -description



  Gets the teletext type code from from a Digital Video Broadcast (DVB) teletext descriptor. 



## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">IDvbTeletextDescriptor::GetCountOfRecords</a>



### -param pbVal [out]

Receives the teletext type code. This can have any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Initial teletext page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Teletext subtitle page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Additional information page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Program schedule page

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
Teletext subtitle page for hearing-impaired people

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x06 - 0x1F</dt>
</dl>
</td>
<td width="60%">
Reserved for future use

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5148a87b-e6b6-4bda-871c-10a2f398ebcc">IDvbTeletextDescriptor</a>



<a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">IDvbTeletextDescriptor::GetCountOfRecords</a>
 

 

