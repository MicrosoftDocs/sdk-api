---
UID: NF:mfidl.IMFTrustedOutput.GetOutputTrustAuthorityCount
title: IMFTrustedOutput::GetOutputTrustAuthorityCount
author: windows-sdk-content
description: Gets the number of output trust authorities (OTAs) provided by this trusted output. Each OTA reports a single action.
old-location: mf\imftrustedoutput_getoutputtrustauthoritycount.htm
tech.root: medfound
ms.assetid: 3aae6859-0b32-4705-9045-b98d0bbf43a6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 3aae6859-0b32-4705-9045-b98d0bbf43a6, GetOutputTrustAuthorityCount, GetOutputTrustAuthorityCount method [Media Foundation], GetOutputTrustAuthorityCount method [Media Foundation],IMFTrustedOutput interface, IMFTrustedOutput interface [Media Foundation],GetOutputTrustAuthorityCount method, IMFTrustedOutput.GetOutputTrustAuthorityCount, IMFTrustedOutput::GetOutputTrustAuthorityCount, mf.imftrustedoutput_getoutputtrustauthoritycount, mfidl/IMFTrustedOutput::GetOutputTrustAuthorityCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFTrustedOutput.GetOutputTrustAuthorityCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTrustedOutput::GetOutputTrustAuthorityCount


## -description


Gets the number of output trust authorities (OTAs) provided by this trusted output. Each OTA reports a single action.


## -parameters




### -param pcOutputTrustAuthorities [out]

Receives the number of OTAs.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/14342d8b-3c76-4c13-8cbe-a60bb66084c8">IMFTrustedOutput</a>
 

 

