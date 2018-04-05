---
UID: NF:atscpsipparser.ISCTE_EAS.GetOriginatorCode
title: ISCTE_EAS::GetOriginatorCode method
author: windows-driver-content
description: The GetOriginatorCode method returns the EAS originator code.
old-location: mstv\iscte_eas_getoriginatorcode.htm
old-project: mstv
ms.assetid: a46f0922-9733-411a-8a03-59e1c98dbdd8
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetOriginatorCode method [Microsoft TV Technologies], GetOriginatorCode method [Microsoft TV Technologies], ISCTE_EAS interface, GetOriginatorCode,ISCTE_EAS.GetOriginatorCode, ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], GetOriginatorCode method, ISCTE_EAS::GetOriginatorCode, ISCTE_EASGetOriginatorCode, atscpsipparser/ISCTE_EAS::GetOriginatorCode, mstv.iscte_eas_getoriginatorcode
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
-	ISCTE_EAS.GetOriginatorCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetOriginatorCode method


## -description


The <b>GetOriginatorCode</b> method returns the EAS originator code.


## -parameters




### -param pbVal [out]


            Receives the EAS_originator_code field.
          


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
 

 

