---
UID: NF:vpconfig.IVPBaseConfig.SetVideoPortID
title: IVPBaseConfig::SetVideoPortID (vpconfig.h)
description: The SetVideoPortID method specifies the ID of the hardware video port to use.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","SetVideoPortID method","IVPBaseConfig.SetVideoPortID","IVPBaseConfig::SetVideoPortID","IVPBaseConfigSetVideoPortID","SetVideoPortID","SetVideoPortID method [DirectShow]","SetVideoPortID method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_setvideoportid","vpconfig/IVPBaseConfig::SetVideoPortID"]
old-location: dshow\ivpbaseconfig_setvideoportid.htm
tech.root: dshow
ms.assetid: 9be16349-b214-4441-8093-dfb0caa84507
ms.date: 12/05/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetVideoPortID method, IVPBaseConfig.SetVideoPortID, IVPBaseConfig::SetVideoPortID, IVPBaseConfigSetVideoPortID, SetVideoPortID, SetVideoPortID method [DirectShow], SetVideoPortID method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setvideoportid, vpconfig/IVPBaseConfig::SetVideoPortID
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPBaseConfig::SetVideoPortID
 - vpconfig/IVPBaseConfig::SetVideoPortID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetVideoPortID
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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>