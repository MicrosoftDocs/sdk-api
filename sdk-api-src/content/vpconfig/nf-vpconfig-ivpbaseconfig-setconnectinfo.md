---
UID: NF:vpconfig.IVPBaseConfig.SetConnectInfo
title: IVPBaseConfig::SetConnectInfo
author: windows-driver-content
description: The SetConnectInfo method sets the video port connection parameters.
old-location: dshow\ivpbaseconfig_setconnectinfo.htm
old-project: DirectShow
ms.assetid: e52bb213-e6e7-4bae-9e1e-6b34f34cf1d1
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetConnectInfo method, IVPBaseConfig.SetConnectInfo, IVPBaseConfig::SetConnectInfo, IVPBaseConfigSetConnectInfo, SetConnectInfo, SetConnectInfo method [DirectShow], SetConnectInfo method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setconnectinfo, vpconfig/IVPBaseConfig::SetConnectInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VMR9VideoStreamInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vpconfig.h
api_name:
-	IVPBaseConfig.SetConnectInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVPBaseConfig::SetConnectInfo


## -description



The <code>SetConnectInfo</code> method sets the video port connection parameters.




## -parameters




### -param dwChosenEntry [in]

Specifies the index of connect information to pass to the driver. The value is a zero-based index into the array returned by the <a href="https://msdn.microsoft.com/b428e77a-83c3-42ce-95e4-1cdde4da066d">IVPBaseConfig::GetConnectInfo</a> method.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

