---
UID: NF:dvbsiparser.IDvbServiceDescriptor2.GetServiceProviderNameW
title: IDvbServiceDescriptor2::GetServiceProviderNameW method
author: windows-driver-content
description: Gets a string containing the service provider name from a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicedescriptor2_getserviceprovidernamew.htm
old-project: mstv
ms.assetid: b0d44251-adef-4a90-b5a3-dc36576169b9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetServiceProviderNameW method [Microsoft TV Technologies], GetServiceProviderNameW method [Microsoft TV Technologies], IDvbServiceDescriptor2 interface, GetServiceProviderNameW,IDvbServiceDescriptor2.GetServiceProviderNameW, IDvbServiceDescriptor2, IDvbServiceDescriptor2 interface [Microsoft TV Technologies], GetServiceProviderNameW method, IDvbServiceDescriptor2::GetServiceProviderNameW, dvbsiparser/IDvbServiceDescriptor2::GetServiceProviderNameW, mstv.idvbservicedescriptor2_getserviceprovidernamew
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
-	IDvbServiceDescriptor2.GetServiceProviderNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbServiceDescriptor2::GetServiceProviderNameW method


## -description


Gets a string containing the service provider name from  a Digital Video Broadcast (DVB) service descriptor. 


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Receives the service provider name string as a <b>BSTR</b>. The caller must free the string by calling <b>SysFreeString</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/795c4a5c-c363-401b-8b26-447903163f80">IDvbServiceDescriptor2</a>
 

 

