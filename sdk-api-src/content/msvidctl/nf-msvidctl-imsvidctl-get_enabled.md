---
UID: NF:msvidctl.IMSVidCtl.get_Enabled
title: IMSVidCtl::get_Enabled (msvidctl.h)
description: The get_Enabled method retrieves a value that determines whether the Video Control can respond to user-generated events.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_Enabled method","IMSVidCtl.get_Enabled","IMSVidCtl::get_Enabled","IMSVidCtlget_Enabled","get_Enabled","get_Enabled method [Microsoft TV Technologies]","get_Enabled method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_enabled","msvidctl/IMSVidCtl::get_Enabled"]
old-location: mstv\imsvidctl_get_enabled.htm
tech.root: mstv
ms.assetid: 7c1ec2a6-9880-4420-8d28-4374f1658bd9
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_Enabled method, IMSVidCtl.get_Enabled, IMSVidCtl::get_Enabled, IMSVidCtlget_Enabled, get_Enabled, get_Enabled method [Microsoft TV Technologies], get_Enabled method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_enabled, msvidctl/IMSVidCtl::get_Enabled
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - IMSVidCtl::get_Enabled
 - msvidctl/IMSVidCtl::get_Enabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_Enabled
---

# IMSVidCtl::get_Enabled


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Enabled</b> method retrieves a value that determines whether the Video Control can respond to user-generated events.

## -parameters

### -param pbool [out]

Variable of type <b>VARIANT_BOOL</b> that receives the current value of the property.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_enabled">IMSVidCtl::put_Enabled</a>