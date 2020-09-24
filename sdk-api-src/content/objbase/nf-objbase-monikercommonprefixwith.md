---
UID: NF:objbase.MonikerCommonPrefixWith
title: MonikerCommonPrefixWith function (objbase.h)
description: Creates a new moniker based on the common prefix that this moniker (the one comprising the data of this moniker object) shares with another moniker.
helpviewer_keywords: ["MonikerCommonPrefixWith","MonikerCommonPrefixWith function [COM]","_com_MonikerCommonPrefixWith","com.monikercommonprefixwith","objbase/MonikerCommonPrefixWith"]
old-location: com\monikercommonprefixwith.htm
tech.root: com
ms.assetid: 6caa8c2e-c3d6-45d5-8efe-74d6a2c4a926
ms.date: 12/05/2018
ms.keywords: MonikerCommonPrefixWith, MonikerCommonPrefixWith function [COM], _com_MonikerCommonPrefixWith, com.monikercommonprefixwith, objbase/MonikerCommonPrefixWith
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MonikerCommonPrefixWith
 - objbase/MonikerCommonPrefixWith
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - MonikerCommonPrefixWith
---

# MonikerCommonPrefixWith function


## -description

Creates a new moniker based on the common prefix that this moniker (the one comprising the data of this moniker object) shares with another moniker.

This function is intended to be called only in implementations of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-commonprefixwith">IMoniker::CommonPrefixWith</a>.

## -parameters

### -param pmkThis [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on one of the monikers for which a common prefix is sought; usually the moniker in which this call is used to implement <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-commonprefixwith">IMoniker::CommonPrefixWith</a>.

### -param pmkOther [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker to be compared with the first moniker.

### -param ppmkCommon [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the moniker based on the common prefix of <i>pmkThis</i> and <i>pmkOther</i>. When successful, the function has called <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the moniker and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. If an error occurs, the supplied interface pointer value is <b>NULL</b>.

## -returns

This function can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
A common prefix exists that is neither <i>pmkThis</i> nor <i>pmkOther</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_HIM</b></dt>
</dl>
</td>
<td width="60%">
The entire <i>pmkOther</i> moniker is a prefix of the <i>pmkThis</i> moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_ME</b></dt>
</dl>
</td>
<td width="60%">
The entire <i>pmkThis</i> moniker is a prefix of the <i>pmkOther</i> moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_S_US</b></dt>
</dl>
</td>
<td width="60%">
The <i>pmkThis</i> and <i>pmkOther</i> monikers are equal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOPREFIX</b></dt>
</dl>
</td>
<td width="60%">
The monikers have no common prefix.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOTBINDABLE</b></dt>
</dl>
</td>
<td width="60%">
This function was called on a relative moniker. It is not meaningful to take the common prefix of relative monikers.

</td>
</tr>
</table>

## -remarks

Your implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-commonprefixwith">IMoniker::CommonPrefixWith</a> should first check whether the other moniker is of a type that you recognize and handle in a special way. If not, you should call <b>MonikerCommonPrefixWith</b>, passing itself as <i>pmkThis</i> and the other moniker as <i>pmkOther</i>. <b>MonikerCommonPrefixWith</b> correctly handles the cases where either moniker is a generic composite. 



You should call this function only if <i>pmkThis</i> and <i>pmkOther</i> are both absolute monikers (where an absolute moniker is either a file moniker or a generic composite whose leftmost component is a file moniker, and where the file moniker represents an absolute path). Do not call this function on relative monikers.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-commonprefixwith">IMoniker::CommonPrefixWith</a>