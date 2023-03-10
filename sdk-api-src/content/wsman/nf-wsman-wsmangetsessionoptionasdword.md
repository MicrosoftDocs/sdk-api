---
UID: NF:wsman.WSManGetSessionOptionAsDword
title: WSManGetSessionOptionAsDword function (wsman.h)
description: Gets the value of a session option. (WSManGetSessionOptionAsDword)
helpviewer_keywords: ["WSManGetSessionOptionAsDword","WSManGetSessionOptionAsDword function [Windows Remote Management]","winrm.wsmangetsessionoptionasdword","wsman/WSManGetSessionOptionAsDword"]
old-location: winrm\wsmangetsessionoptionasdword.htm
tech.root: winrm
ms.assetid: 73ff4a3a-89f7-4362-99fb-7423e3fd853f
ms.date: 12/05/2018
ms.keywords: WSManGetSessionOptionAsDword, WSManGetSessionOptionAsDword function [Windows Remote Management], winrm.wsmangetsessionoptionasdword, wsman/WSManGetSessionOptionAsDword
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManGetSessionOptionAsDword
 - wsman/WSManGetSessionOptionAsDword
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManGetSessionOptionAsDword
---

# WSManGetSessionOptionAsDword function


## -description

Gets the value of a session option.

## -parameters

### -param session [in]

Specifies the handle returned by a <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreatesession">WSManCreateSession</a> call.  This parameter cannot be <b>NULL</b>.

### -param option

Specifies the option to get. Not all session options can be retrieved. The options are defined in the <a href="/windows/desktop/api/wsman/ne-wsman-wsmansessionoption">WSManSessionOption</a> enumeration.

### -param value [in, out]

Specifies the value of specified session option.

## -returns

This method returns zero on success. Otherwise, this method returns an error code.
