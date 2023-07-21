---
UID: NF:msvidctl.IMSVidCtl.put_Enabled
title: IMSVidCtl::put_Enabled (msvidctl.h)
description: The put_Enabled method specifies a value that determines whether the Video Control can respond to user-generated events.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_Enabled method","IMSVidCtl.put_Enabled","IMSVidCtl::put_Enabled","IMSVidCtlput_Enabled","mstv.imsvidctl_put_enabled","msvidctl/IMSVidCtl::put_Enabled","put_Enabled","put_Enabled method [Microsoft TV Technologies]","put_Enabled method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_enabled.htm
tech.root: mstv
ms.assetid: 366164ac-1514-46d6-870a-388706b8de75
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_Enabled method, IMSVidCtl.put_Enabled, IMSVidCtl::put_Enabled, IMSVidCtlput_Enabled, mstv.imsvidctl_put_enabled, msvidctl/IMSVidCtl::put_Enabled, put_Enabled, put_Enabled method [Microsoft TV Technologies], put_Enabled method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_Enabled
 - msvidctl/IMSVidCtl::put_Enabled
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
 - IMSVidCtl.put_Enabled
---

# IMSVidCtl::put_Enabled


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Enabled</b> method specifies a value that determines whether the Video Control can respond to user-generated events.

## -parameters

### -param vbool [in]

Specifies the new value of the property.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_enabled">IMSVidCtl::get_Enabled</a>