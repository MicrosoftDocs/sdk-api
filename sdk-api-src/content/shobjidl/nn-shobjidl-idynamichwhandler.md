---
UID: NN:shobjidl.IDynamicHWHandler
title: IDynamicHWHandler (shobjidl.h)
description: Called by AutoPlay. Exposes methods that get dynamic information regarding a registered handler prior to displaying it to the user.
helpviewer_keywords: ["IDynamicHWHandler","IDynamicHWHandler interface [Windows Shell]","IDynamicHWHandler interface [Windows Shell]","described","_shell_IDynamicHWHandler","shell.IDynamicHWHandler","shobjidl/IDynamicHWHandler"]
old-location: shell\IDynamicHWHandler.htm
tech.root: shell
ms.assetid: 924a765f-76b2-4a45-8dc5-74b5e75b437d
ms.date: 12/05/2018
ms.keywords: IDynamicHWHandler, IDynamicHWHandler interface [Windows Shell], IDynamicHWHandler interface [Windows Shell],described, _shell_IDynamicHWHandler, shell.IDynamicHWHandler, shobjidl/IDynamicHWHandler
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IDynamicHWHandler
 - shobjidl/IDynamicHWHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IDynamicHWHandler
---

# IDynamicHWHandler interface


## -description

Called by AutoPlay. Exposes methods that get dynamic information regarding a registered handler prior to displaying it to the user.

## -inheritance

The <b>IDynamicHWHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDynamicHWHandler</b> also has these types of members:

## -remarks

Prior to this interface, when an application registered a handler and was displayed in the autoplay prompt, the handler was always shown as long as the content type (for example, mp3 or avi) associated with that handler was found on the media device. The same icon and action string were always displayed.

If a handler implements this interface prior to showing the handler,  AutoPlay will first call <a href="/windows/desktop/api/shobjidl/nf-shobjidl-idynamichwhandler-getdynamicinfo">IDynamicHWHandler::GetDynamicInfo</a> to determine if this handler is to be presented to the user. If you want to show the handler, you may specify a different action string than the one supplied by the static handler registration under <b>HKLM</b>.
