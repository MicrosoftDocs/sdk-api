---
UID: NF:winuser.GetUnpredictedMessagePos
title: GetUnpredictedMessagePos function (winuser.h)
description: Gets pointer data before it has gone through touch prediction processing.
helpviewer_keywords: ["GetUnpredictedMessagePos","GetUnpredictedMessagePos function [Input Messages and Notifications]","inputmsg.getunpredictedmessagepos","winuser/GetUnpredictedMessagePos"]
old-location: inputmsg\getunpredictedmessagepos.htm
tech.root: InputMsg
ms.assetid: 5BE2748B-0124-4647-A77E-EA2937C7B1AD
ms.date: 12/05/2018
ms.keywords: GetUnpredictedMessagePos, GetUnpredictedMessagePos function [Input Messages and Notifications], inputmsg.getunpredictedmessagepos, winuser/GetUnpredictedMessagePos
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetUnpredictedMessagePos
 - winuser/GetUnpredictedMessagePos
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetUnpredictedMessagePos
---

# GetUnpredictedMessagePos function


## -description

Gets pointer data before it has gone through touch prediction processing.



## -returns

The screen location of the pointer input.

## -remarks

By default, touch prediction is activated.

## -see-also

<a href="/windows/win32/inputmsg/functions">Functions</a>



<a href="/windows/desktop/api/winuser/ns-winuser-touchpredictionparameters">TouchPredictionParameters</a>
