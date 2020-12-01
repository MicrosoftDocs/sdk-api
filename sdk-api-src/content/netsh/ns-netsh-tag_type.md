---
UID: NS:netsh._TAG_TYPE
title: TAG_TYPE (netsh.h)
description: Specifies tags used for the PreprocessCommand function.
helpviewer_keywords: ["*PTAG_TYPE","NS_REQ_ALLOW_MULTIPLE","NS_REQ_ONE_OR_MORE","NS_REQ_PRESENT","NS_REQ_ZERO","PTAG_TYPE","PTAG_TYPE structure pointer [NetShell]","TAG_TYPE","TAG_TYPE structure [NetShell]","_netsh_tag_type","netsh/PTAG_TYPE","netsh/TAG_TYPE","netshell.tag_type"]
old-location: netshell\tag_type.htm
tech.root: netshell
ms.assetid: 3e87447e-5374-4411-96ab-3ad400948aa5
ms.date: 12/05/2018
ms.keywords: '*PTAG_TYPE, NS_REQ_ALLOW_MULTIPLE, NS_REQ_ONE_OR_MORE, NS_REQ_PRESENT, NS_REQ_ZERO, PTAG_TYPE, PTAG_TYPE structure pointer [NetShell], TAG_TYPE, TAG_TYPE structure [NetShell], _netsh_tag_type, netsh/PTAG_TYPE, netsh/TAG_TYPE, netshell.tag_type'
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TAG_TYPE, *PTAG_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TAG_TYPE
 - netsh/_TAG_TYPE
 - PTAG_TYPE
 - netsh/PTAG_TYPE
 - TAG_TYPE
 - netsh/TAG_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netsh.h
api_name:
 - TAG_TYPE
---

# TAG_TYPE structure


## -description

The 
<b>TAG_TYPE</b> structure specifies tags used for the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-preprocesscommand">PreprocessCommand</a> function.

## -struct-fields

### -field pwszTag

A tag string, in UNICODE.

### -field dwRequired

Specifies whether the tag is required.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_ZERO"></a><a id="ns_req_zero"></a><dl>
<dt><b>NS_REQ_ZERO</b></dt>
</dl>
</td>
<td width="60%">
Tag is optional.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_PRESENT"></a><a id="ns_req_present"></a><dl>
<dt><b>NS_REQ_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
Tag must be present.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_ALLOW_MULTIPLE"></a><a id="ns_req_allow_multiple"></a><dl>
<dt><b>NS_REQ_ALLOW_MULTIPLE</b></dt>
</dl>
</td>
<td width="60%">
Multiple copies of the tag is allowed.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_ONE_OR_MORE"></a><a id="ns_req_one_or_more"></a><dl>
<dt><b>NS_REQ_ONE_OR_MORE</b></dt>
</dl>
</td>
<td width="60%">
Multiple copies of the tag is allowed. Tag must be present.

</td>
</tr>
</table>

### -field bPresent

This value specifies whether the tag is present. <b>TRUE</b> indicates the tag is present.



## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-preprocesscommand">PreprocessCommand</a>