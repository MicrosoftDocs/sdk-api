---
UID: NF:mfidl.IMFTrustedOutput.GetOutputTrustAuthorityByIndex
title: IMFTrustedOutput::GetOutputTrustAuthorityByIndex (mfidl.h)
author: windows-sdk-content
description: Gets an output trust authority (OTA), specified by index.
old-location: mf\imftrustedoutput_getoutputtrustauthoritybyindex.htm
tech.root: medfound
ms.assetid: 4dd570e7-c6fb-4ffb-8ef5-b88a6638dbbf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 4dd570e7-c6fb-4ffb-8ef5-b88a6638dbbf, GetOutputTrustAuthorityByIndex, GetOutputTrustAuthorityByIndex method [Media Foundation], GetOutputTrustAuthorityByIndex method [Media Foundation],IMFTrustedOutput interface, IMFTrustedOutput interface [Media Foundation],GetOutputTrustAuthorityByIndex method, IMFTrustedOutput.GetOutputTrustAuthorityByIndex, IMFTrustedOutput::GetOutputTrustAuthorityByIndex, mf.imftrustedoutput_getoutputtrustauthoritybyindex, mfidl/IMFTrustedOutput::GetOutputTrustAuthorityByIndex
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTrustedOutput.GetOutputTrustAuthorityByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTrustedOutput::GetOutputTrustAuthorityByIndex


## -description


Gets an output trust authority (OTA), specified by index.


## -parameters




### -param dwIndex [in]

Zero-based index of the OTA to retrieve. To get the number of OTAs provided by this object, call <a href="https://msdn.microsoft.com/3aae6859-0b32-4705-9045-b98d0bbf43a6">IMFTrustedOutput::GetOutputTrustAuthorityCount</a>.
          


### -param ppauthority [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/21594ac0-7e3c-44a3-bbee-64316dd51824">IMFOutputTrustAuthority</a> interface of the OTA. The caller must release the interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/14342d8b-3c76-4c13-8cbe-a60bb66084c8">IMFTrustedOutput</a>
 

 

