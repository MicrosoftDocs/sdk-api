---
UID: NF:shobjidl_core.IAssocHandler.IsRecommended
title: IAssocHandler::IsRecommended (shobjidl_core.h)
description: Indicates whether the application is registered as a recommended handler for the queried file type.
helpviewer_keywords: ["IAssocHandler interface [Windows Shell]","IsRecommended method","IAssocHandler.IsRecommended","IAssocHandler::IsRecommended","IsRecommended","IsRecommended method [Windows Shell]","IsRecommended method [Windows Shell]","IAssocHandler interface","_shell_IAssocHandler_IsRecommended","shell.IAssocHandler_IsRecommended","shobjidl_core/IAssocHandler::IsRecommended"]
old-location: shell\IAssocHandler_IsRecommended.htm
tech.root: shell
ms.assetid: 3c312db3-a656-436c-a012-669553355fa5
ms.date: 12/05/2018
ms.keywords: IAssocHandler interface [Windows Shell],IsRecommended method, IAssocHandler.IsRecommended, IAssocHandler::IsRecommended, IsRecommended, IsRecommended method [Windows Shell], IsRecommended method [Windows Shell],IAssocHandler interface, _shell_IAssocHandler_IsRecommended, shell.IAssocHandler_IsRecommended, shobjidl_core/IAssocHandler::IsRecommended
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IAssocHandler::IsRecommended
 - shobjidl_core/IAssocHandler::IsRecommended
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAssocHandler.IsRecommended
---

# IAssocHandler::IsRecommended


## -description

Indicates whether the application is registered as a recommended handler for the queried file type.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the program is recommended; otherwise, S_FALSE.

## -remarks

Applications that register themselves as handlers for particular file types can specify whether they are recommended handlers. This has no effect on the actual behavior of the applications when launched. It is simply provided as a hint to the user and a value that the UI can utilize programmatically, if desired. For example, the Shell's <b>Open With</b> dialog separates entries into <b>Recommended Programs</b> and <b>Other Programs</b>.

Note that program recommendations may change over time. One example is provided when the user chooses an application from the <b>Other Programs</b> of the <b>Open With</b> dialog to open a particular file type. That may cause the Shell to "promote" that application to recommended status for that file type. Because the recommended status may change over time, applications should not cache this value, but query it each time it is needed.

If <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers">SHAssocEnumHandlers</a> was called with the ASSOC_FILTER_RECOMMENDED flag, then only recommended handlers are returned. If the ASSOC_FILTER_NONE flag was used, then you must call <b>IAssocHandler::IsRecommended</b> on each <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a> object to determine whether it is recommended or not.
