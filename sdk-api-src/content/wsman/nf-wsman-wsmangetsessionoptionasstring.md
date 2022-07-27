---
UID: NF:wsman.WSManGetSessionOptionAsString
title: WSManGetSessionOptionAsString function (wsman.h)
description: Gets the value of a session option. (WSManGetSessionOptionAsString)
helpviewer_keywords: ["WSManGetSessionOptionAsString","WSManGetSessionOptionAsString function [Windows Remote Management]","winrm.wsmangetsessionoptionasstring","wsman/WSManGetSessionOptionAsString"]
old-location: winrm\wsmangetsessionoptionasstring.htm
tech.root: winrm
ms.assetid: 7fb1cec5-059f-4710-868a-d34c6ae2fd2a
ms.date: 12/05/2018
ms.keywords: WSManGetSessionOptionAsString, WSManGetSessionOptionAsString function [Windows Remote Management], winrm.wsmangetsessionoptionasstring, wsman/WSManGetSessionOptionAsString
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
 - WSManGetSessionOptionAsString
 - wsman/WSManGetSessionOptionAsString
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
 - WSManGetSessionOptionAsString
---

# WSManGetSessionOptionAsString function


## -description

Gets the value of a session option.

## -parameters

### -param session [in]

Specifies the session handle returned by a  <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreatesession">WSManCreateSession</a> call.  This parameter cannot be <b>NULL</b>.

### -param option

Specifies the option to get. Not all session options can be retrieved. The values for the options are defined in the <a href="/windows/desktop/api/wsman/ne-wsman-wsmansessionoption">WSManSessionOption</a> enumeration.

### -param stringLength

Specifies the length of the storage location for <i>string</i> parameter.

### -param string [out, optional]

A pointer to the storage location for the value of the specified session option.

### -param stringLengthUsed [out]

Specifies the length of the string returned in the <i>string</i> parameter.

## -returns

This method returns zero on success. Otherwise, this method returns an error code.
