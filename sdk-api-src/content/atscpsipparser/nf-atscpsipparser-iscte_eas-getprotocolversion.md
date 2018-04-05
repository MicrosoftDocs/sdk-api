---
UID: NF:atscpsipparser.ISCTE_EAS.GetProtocolVersion
title: ISCTE_EAS::GetProtocolVersion method
author: windows-driver-content
description: The GetProtocolVersion method returns the protocol version of the EAS table.
old-location: mstv\iscte_eas_getprotocolversion.htm
old-project: mstv
ms.assetid: 80700a74-85d6-4269-9000-83e62f68aeb1
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetProtocolVersion method [Microsoft TV Technologies], GetProtocolVersion method [Microsoft TV Technologies], ISCTE_EAS interface, GetProtocolVersion,ISCTE_EAS.GetProtocolVersion, ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], GetProtocolVersion method, ISCTE_EAS::GetProtocolVersion, ISCTE_EASGetProtocolVersion, atscpsipparser/ISCTE_EAS::GetProtocolVersion, mstv.iscte_eas_getprotocolversion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: APPX_PACKAGE_WRITER_PAYLOAD_STREAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	ISCTE_EAS.GetProtocolVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetProtocolVersion method


## -description


The <b>GetProtocolVersion</b> method returns the protocol version of the EAS table.


## -parameters




### -param pbVal [out]


            Receives the protocol_version field.
          


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
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/f40e89f4-6a33-44a9-933c-bf38978f1cb2">ISCTE_EAS::Initialize</a> method was not called.

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




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS Interface</a>
 

 

