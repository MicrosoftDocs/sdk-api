---
UID: NN:shobjidl.IUserNotification2
title: IUserNotification2 (shobjidl.h)
description: Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar. (IUserNotification2)
helpviewer_keywords: ["IUserNotification2","IUserNotification2 interface [Windows Shell]","IUserNotification2 interface [Windows Shell]","described","_shell_IUserNotification2","shell.IUserNotification2","shobjidl/IUserNotification2"]
old-location: shell\IUserNotification2.htm
tech.root: shell
ms.assetid: 6605a014-4f79-4856-8fd9-df926ea76052
ms.date: 12/05/2018
ms.keywords: IUserNotification2, IUserNotification2 interface [Windows Shell], IUserNotification2 interface [Windows Shell],described, _shell_IUserNotification2, shell.IUserNotification2, shobjidl/IUserNotification2
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
req.dll: Shell32.dll (version 6.0.6 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserNotification2
 - shobjidl/IUserNotification2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IUserNotification2
---

# IUserNotification2 interface


## -description

Exposes methods that set notification information and then display that notification to the user in a balloon that appears in conjunction with the notification area of the taskbar.
            
            
<div class="alert"><b>Note</b>  <b>IUserNotification2</b> does not inherit from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification">IUserNotification</a>. <b>IUserNotification2</b> differs from <b>IUserNotification</b> only in its <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iusernotification2-show">Show</a> method, which adds an additional parameter for a callback interface to communicate with the notification. Otherwise the two interfaces are identical in form and function. CLSID_UserNotification implements both versions of <b>Show</b> as an overload.</div><div> </div>

## -inheritance

The <b>IUserNotification2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUserNotification2</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_UserNotification.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification">IUserNotification</a>
