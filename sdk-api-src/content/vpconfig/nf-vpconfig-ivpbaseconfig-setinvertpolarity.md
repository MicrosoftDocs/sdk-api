---
UID: NF:vpconfig.IVPBaseConfig.SetInvertPolarity
title: IVPBaseConfig::SetInvertPolarity
author: windows-sdk-content
description: The SetInvertPolarity method reverses the current polarity the device uses.
old-location: dshow\ivpbaseconfig_setinvertpolarity.htm
tech.root: DirectShow
ms.assetid: 2c33cea2-2c83-4978-9059-c15706f14f85
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetInvertPolarity method, IVPBaseConfig.SetInvertPolarity, IVPBaseConfig::SetInvertPolarity, IVPBaseConfigSetInvertPolarity, SetInvertPolarity, SetInvertPolarity method [DirectShow], SetInvertPolarity method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setinvertpolarity, vpconfig/IVPBaseConfig::SetInvertPolarity
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
 - IVPBaseConfig.SetInvertPolarity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::SetInvertPolarity


## -description



The <code>SetInvertPolarity</code> method reverses the current polarity the device uses.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Reversing polarity means asking the decoder or capture device to treat even fields as odd fields and vice versa.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

