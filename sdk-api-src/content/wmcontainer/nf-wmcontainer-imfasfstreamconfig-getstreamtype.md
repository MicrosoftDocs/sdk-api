---
UID: NF:wmcontainer.IMFASFStreamConfig.GetStreamType
title: IMFASFStreamConfig::GetStreamType (wmcontainer.h)
author: windows-sdk-content
description: Gets the major media type of the stream.
old-location: mf\imfasfstreamconfig_getstreamtype.htm
tech.root: medfound
ms.assetid: 5f085107-f205-47ab-acb5-d45a881ce76c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5f085107-f205-47ab-acb5-d45a881ce76c, GetStreamType, GetStreamType method [Media Foundation], GetStreamType method [Media Foundation],IMFASFStreamConfig interface, IMFASFStreamConfig interface [Media Foundation],GetStreamType method, IMFASFStreamConfig.GetStreamType, IMFASFStreamConfig::GetStreamType, mf.imfasfstreamconfig_getstreamtype, wmcontainer/IMFASFStreamConfig::GetStreamType
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFASFStreamConfig.GetStreamType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFStreamConfig::GetStreamType


## -description


Gets the major media type of the stream.
        


## -parameters




### -param pguidStreamType [out]

Receives the major media type for the stream. For a list of possible values, see <a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Major Media Types</a>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>



<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>
 

 

