---
UID: NF:vpconfig.IVPBaseConfig.SetConnectInfo
title: IVPBaseConfig::SetConnectInfo
author: windows-sdk-content
description: The SetConnectInfo method sets the video port connection parameters.
old-location: dshow\ivpbaseconfig_setconnectinfo.htm
tech.root: DirectShow
ms.assetid: e52bb213-e6e7-4bae-9e1e-6b34f34cf1d1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetConnectInfo method, IVPBaseConfig.SetConnectInfo, IVPBaseConfig::SetConnectInfo, IVPBaseConfigSetConnectInfo, SetConnectInfo, SetConnectInfo method [DirectShow], SetConnectInfo method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setconnectinfo, vpconfig/IVPBaseConfig::SetConnectInfo
ms.topic: method
req.header: vpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetConnectInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::SetConnectInfo


## -description



The <code>SetConnectInfo</code> method sets the video port connection parameters.




## -parameters




### -param dwChosenEntry [in]

Specifies the index of connect information to pass to the driver. The value is a zero-based index into the array returned by the <a href="https://msdn.microsoft.com/en-us/library/Dd390568(v=VS.85).aspx">IVPBaseConfig::GetConnectInfo</a> method.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig Interface</a>
 

 

