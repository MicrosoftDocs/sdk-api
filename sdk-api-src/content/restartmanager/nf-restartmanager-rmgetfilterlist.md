---
UID: NF:restartmanager.RmGetFilterList
title: RmGetFilterList function (restartmanager.h)
description: Lists the modifications to shutdown and restart actions that have already been applied by the RmAddFilter function.
helpviewer_keywords: ["RmGetFilterList","RmGetFilterList function [Restart Mgr]","restartmanager/RmGetFilterList","rstmgr.rmgetfilterlist"]
old-location: rstmgr\rmgetfilterlist.htm
tech.root: rstmgr
ms.assetid: 61427838-8b23-4105-93fd-55f457fd43a7
ms.date: 12/05/2018
ms.keywords: RmGetFilterList, RmGetFilterList function [Restart Mgr], restartmanager/RmGetFilterList, rstmgr.rmgetfilterlist
req.header: restartmanager.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rstrtmgr.lib
req.dll: Rstrtmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RmGetFilterList
 - restartmanager/RmGetFilterList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rstrtmgr.dll
api_name:
 - RmGetFilterList
---

# RmGetFilterList function


## -description

Lists the modifications to shutdown and restart actions that have already been applied by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a> function. The function returns a pointer to a buffer containing information about the modifications which have been applied.

## -parameters

### -param dwSessionHandle [in]

A handle to an existing Restart Manager session.

### -param pbFilterBuf [out, optional]

A pointer to a buffer that contains modification information.

### -param cbFilterBuf [in]

The size of the buffer that contains modification information in bytes.

### -param cbFilterBufNeeded [out]

The number of bytes needed in the buffer.

## -returns

This is the most recent error received. The function can return one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a> that are defined in Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
<dt>160</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not correct. This error value is returned by the Restart Manager function if a <b>NULL</b> pointer or 0 is passed in as a parameter that requires a non-<b>null</b> and non-zero value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234</dt>
</dl>
</td>
<td width="60%">
This error value is returned by the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetfilterlist">RmGetFilterList</a> function if the <i>pbFilterBuf</i> buffer is too small to hold all the application information in the list or if <i>cbFilterBufNeeded</i> was not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SESSION_CREDENTIAL_CONFLICT</b></dt>
<dt> 1219</dt>
</dl>
</td>
<td width="60%">
This error is returned when a secondary installer calls this function. This function is only available to primary installers.

</td>
</tr>
</table>

## -remarks

The returned <i>pbFilterBuf</i> buffer has to be typecast to <b>RM_FILTER_INFO</b> to access the filter list.

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a>