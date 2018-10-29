---
UID: NS:wincrypt._CTL_USAGE_MATCH
title: "_CTL_USAGE_MATCH"
author: windows-sdk-content
description: Provides parameters for finding certificate trust lists (CTL) used to build a certificate chain.
old-location: security\ctl_usage_match.htm
tech.root: seccrypto
ms.assetid: 0b1146b7-a6fe-4cd0-aff7-b49ec6f561a0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PCTL_USAGE_MATCH, CTL_USAGE_MATCH, CTL_USAGE_MATCH structure [Security], PCTL_USAGE_MATCH, PCTL_USAGE_MATCH structure pointer [Security], USAGE_MATCH_TYPE_AND, USAGE_MATCH_TYPE_OR, _CTL_USAGE_MATCH, _crypto2_ctl_usage_match, security.ctl_usage_match, wincrypt/CTL_USAGE_MATCH, wincrypt/PCTL_USAGE_MATCH"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CTL_USAGE_MATCH
product: Windows
targetos: Windows
req.typenames: CTL_USAGE_MATCH, *PCTL_USAGE_MATCH
req.redist: 
---

# _CTL_USAGE_MATCH structure


## -description


The <b>CTL_USAGE_MATCH</b> structure provides parameters for finding <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust lists</a> (CTL) used to build a certificate chain.


## -struct-fields




### -field dwType

Determines the kind of issuer matching to be done. In <b>AND</b> logic, the certificate must meet all criteria. In <b>OR</b> logic, the certificate must meet at least one of the criteria. The following codes are defined to determine the logic used in the match.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USAGE_MATCH_TYPE_AND"></a><a id="usage_match_type_and"></a><dl>
<dt><b>USAGE_MATCH_TYPE_AND</b></dt>
</dl>
</td>
<td width="60%">
<b>AND</b> logic

</td>
</tr>
<tr>
<td width="40%"><a id="USAGE_MATCH_TYPE_OR"></a><a id="usage_match_type_or"></a><dl>
<dt><b>USAGE_MATCH_TYPE_OR</b></dt>
</dl>
</td>
<td width="60%">
<b>OR</b> logic

</td>
</tr>
</table>
 

Default usage match logic is USAGE_MATCH_TYPE_AND.


### -field Usage


<a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CTL_USAGE</a> structure that includes an array of <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) a CTL must match in order to be valid.

