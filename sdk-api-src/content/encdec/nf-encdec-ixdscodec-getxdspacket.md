---
UID: NF:encdec.IXDSCodec.GetXDSPacket
title: IXDSCodec::GetXDSPacket method
author: windows-driver-content
description: The GetXDSPacket method retrieves the most recent XDS packet.
old-location: mstv\ixdscodec_getxdspacket.htm
old-project: mstv
ms.assetid: 44a74489-4ed7-42f0-b8d5-bf86e0f7072c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetXDSPacket method [Microsoft TV Technologies], GetXDSPacket method [Microsoft TV Technologies], IXDSCodec interface, GetXDSPacket,IXDSCodec.GetXDSPacket, IXDSCodec, IXDSCodec interface [Microsoft TV Technologies], GetXDSPacket method, IXDSCodec::GetXDSPacket, IXDSCodecGetXDSPacket, encdec/IXDSCodec::GetXDSPacket, mstv.ixdscodec_getxdspacket
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IXDSCodec.GetXDSPacket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IXDSCodec::GetXDSPacket method


## -description


The <b>GetXDSPacket</b> method retrieves the most recent XDS packet.


## -parameters




### -param pXDSClassPkt [out]

Receives the packet class.


### -param pXDSTypePkt [out]

Receives the class-specific packet type.


### -param pBstrXDSPkt [out]

Receives the packet as a <b>BSTR</b> value.


### -param pPktSeqID [out]

Receives the number of ratings packets that have been decoded. This information can be used for diagnostic purposes.


### -param pCallSeqID [out]

Receives the number of times this method has been called for the current ratings packet. This information can be used for diagnostic purposes.


### -param pTimeStart [out]

Receives the start time of the sample containing the packet.


### -param pTimeEnd [out]

Receives the stop time of the sample containing the packet.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



The returned <b>BSTR</b> contains binary data which might include embedded NULL characters. The caller must free the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/c34a3418-2ae5-45a6-9e3b-2bd7cf33d44b">IXDSCodec Interface</a>
 

 

