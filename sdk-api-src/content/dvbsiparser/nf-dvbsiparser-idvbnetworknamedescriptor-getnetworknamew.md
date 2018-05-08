---
UID: NF:dvbsiparser.IDvbNetworkNameDescriptor.GetNetworkNameW
title: IDvbNetworkNameDescriptor::GetNetworkNameW
author: windows-driver-content
description: Gets the network name, in Unicode string format, from a Digital Video Broadcast (DVB) network name descriptor.
old-location: mstv\idvbnetworknamedescriptor_getnetworknamew.htm
old-project: mstv
ms.assetid: 2c7e1507-2b55-468d-b83d-643a45118429
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetNetworkNameW, GetNetworkNameW method [Microsoft TV Technologies], GetNetworkNameW method [Microsoft TV Technologies],IDvbNetworkNameDescriptor interface, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],GetNetworkNameW method, IDvbNetworkNameDescriptor.GetNetworkNameW, IDvbNetworkNameDescriptor::GetNetworkNameW, dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkNameW, mstv.idvbnetworknamedescriptor_getnetworknamew
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbNetworkNameDescriptor.GetNetworkNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbNetworkNameDescriptor::GetNetworkNameW


## -description


Gets the network name, in Unicode string format, from a Digital Video Broadcast (DVB) network name descriptor.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to a string buffer that receives the network name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b80892d-05e6-4776-932a-a9e2bf985984">IDvbNetworkNameDescriptor</a>
 

 

