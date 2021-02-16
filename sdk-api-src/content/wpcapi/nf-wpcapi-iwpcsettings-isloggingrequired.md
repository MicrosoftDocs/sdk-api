---
UID: NF:wpcapi.IWPCSettings.IsLoggingRequired
title: IWPCSettings::IsLoggingRequired (wpcapi.h)
description: Determines whether activity logging should be performed when obtaining the IWPCSettings interface.
helpviewer_keywords: ["IWPCSettings interface","IsLoggingRequired method","IWPCSettings.IsLoggingRequired","IWPCSettings::IsLoggingRequired","IsLoggingRequired","IsLoggingRequired method","IsLoggingRequired method","IWPCSettings interface","parcon.iwpcsettings_isloggingrequired","wpcapi/IWPCSettings::IsLoggingRequired"]
old-location: parcon\iwpcsettings_isloggingrequired.htm
tech.root: parcon
ms.assetid: bfe04843-af23-4146-bc45-f91d6ad36c1a
ms.date: 12/05/2018
ms.keywords: IWPCSettings interface,IsLoggingRequired method, IWPCSettings.IsLoggingRequired, IWPCSettings::IsLoggingRequired, IsLoggingRequired, IsLoggingRequired method, IsLoggingRequired method,IWPCSettings interface, parcon.iwpcsettings_isloggingrequired, wpcapi/IWPCSettings::IsLoggingRequired
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - IWPCSettings::IsLoggingRequired
 - wpcapi/IWPCSettings::IsLoggingRequired
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCSettings.IsLoggingRequired
---

# IWPCSettings::IsLoggingRequired


## -description

Determines whether activity logging should be performed when obtaining the <a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcsettings">IWPCSettings</a> interface.

## -parameters

### -param pfRequired [out]

Indicates whether logging is required.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process has insufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The user settings were not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcsettings">IWPCSettings</a>