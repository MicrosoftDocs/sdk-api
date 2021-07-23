---
UID: NN:shobjidl.IQueryCancelAutoPlay
title: IQueryCancelAutoPlay (shobjidl.h)
description: Exposes a method that programmatically overrides AutoPlay or AutoRun. This allows you to customize the location and type of content that is launched when media is inserted.
helpviewer_keywords: ["IQueryCancelAutoPlay","IQueryCancelAutoPlay interface [Windows Shell]","IQueryCancelAutoPlay interface [Windows Shell]","described","_shell_IQueryCancelAutoPlay","shell.IQueryCancelAutoPlay","shobjidl/IQueryCancelAutoPlay"]
old-location: shell\IQueryCancelAutoPlay.htm
tech.root: shell
ms.assetid: 7dd470cd-163b-43e1-80d9-cdaa8b615858
ms.date: 12/05/2018
ms.keywords: IQueryCancelAutoPlay, IQueryCancelAutoPlay interface [Windows Shell], IQueryCancelAutoPlay interface [Windows Shell],described, _shell_IQueryCancelAutoPlay, shell.IQueryCancelAutoPlay, shobjidl/IQueryCancelAutoPlay
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryCancelAutoPlay
 - shobjidl/IQueryCancelAutoPlay
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
 - IQueryCancelAutoPlay
---

# IQueryCancelAutoPlay interface


## -description

Exposes a method that programmatically overrides <a href="/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)">AutoPlay</a> or <a href="/previous-versions/windows/desktop/legacy/cc144202(v=vs.85)">AutoRun</a>. This allows you to customize the location and type of content that is launched when media is inserted.

## -inheritance

The <b>IQueryCancelAutoPlay</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryCancelAutoPlay</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  <b>IQueryCancelAutoPlay</b> is intended only for use by user-launched applications that are currently running. It should not be handled by invisible or background service applications to prevent the normal AutoPlay/AutoRun feature from being invoked. Giving the user a choice of what happens when media and devices are inserted into the system is a key feature of the platform. This feature is designed specifically to improve and personalize the user experience and should not be inhibited by background services.</div>
<div> </div>
A valid use of <b>IQueryCancelAutoPlay</b> is illustrated in the following scenario: Assume that you have, through AutoPlay, previously designated application A to handle video camera events. For video editing, however, you prefer application B. You open application B, begin editing some previously filmed video, and then decide to add some new content to the video being edited. Application B's import function prompts you to turn on the video camera so that the new content can be accessed. Normally, this video device activation would trigger the launch of the device-associated application A. Fortunately, using <b>IQueryCancelAutoPlay</b>, application B has canceled AutoPlay processing of video camera events while you are editing video content. In this case, the cancellation of Autoplay by application B has created a better user experience.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/cc144202(v=vs.85)">Autoplay in Windows XP: Automatically Detect and React to New Devices on a System</a>
