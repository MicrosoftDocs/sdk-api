---
UID: NF:vpconfig.IVPBaseConfig.GetVPDataInfo
title: IVPBaseConfig::GetVPDataInfo
author: windows-sdk-content
description: The GetVPDataInfo method retrieves the current video port data information.
old-location: dshow\ivpbaseconfig_getvpdatainfo.htm
tech.root: DirectShow
ms.assetid: 385ab5e4-b904-4268-a97e-1c3e7789b0a2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVPDataInfo, GetVPDataInfo method [DirectShow], GetVPDataInfo method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetVPDataInfo method, IVPBaseConfig.GetVPDataInfo, IVPBaseConfig::GetVPDataInfo, IVPBaseConfigGetVPDataInfo, dshow.ivpbaseconfig_getvpdatainfo, vpconfig/IVPBaseConfig::GetVPDataInfo
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
 - IVPBaseConfig.GetVPDataInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::GetVPDataInfo


## -description



The <code>GetVPDataInfo</code> method retrieves the current video port data information.




## -parameters




### -param pamvpDataInfo [in, out]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd373450(v=VS.85).aspx">AMVPDATAINFO</a> structure allocated by the caller. The device fills in the structure with information about the video port.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig Interface</a>
 

 

