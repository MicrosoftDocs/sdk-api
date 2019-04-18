---
UID: NF:vpconfig.IVPBaseConfig.SetVideoPortID
title: IVPBaseConfig::SetVideoPortID (vpconfig.h)
author: windows-sdk-content
description: The SetVideoPortID method specifies the ID of the hardware video port to use.
old-location: dshow\ivpbaseconfig_setvideoportid.htm
tech.root: DirectShow
ms.assetid: 9be16349-b214-4441-8093-dfb0caa84507
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetVideoPortID method, IVPBaseConfig.SetVideoPortID, IVPBaseConfig::SetVideoPortID, IVPBaseConfigSetVideoPortID, SetVideoPortID, SetVideoPortID method [DirectShow], SetVideoPortID method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setvideoportid, vpconfig/IVPBaseConfig::SetVideoPortID
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
 - IVPBaseConfig.SetVideoPortID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVPBaseConfig::SetVideoPortID


## -description



The <code>SetVideoPortID</code> method specifies the ID of the hardware video port to use.




## -parameters




### -param dwVideoPortID [in]

Specifies the video port ID. This value corresponds to the <b>dwVideoPortID</b> member of the <b>DDVIDEOPORTDESC</b> structure, which is documented in the Windows DDK.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method sets the DirectDraw video port ID on the mini driver to enable it to communicate with the video port directly.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig Interface</a>
 

 

