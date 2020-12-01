---
UID: NF:objbase.CoInstall
title: CoInstall function (objbase.h)
description: Installs the requested COM server application.
helpviewer_keywords: ["CoInstall","CoInstall function [Windows API]","objbase/CoInstall","winprog.coinstall"]
old-location: winprog\coinstall.htm
tech.root: winprog
ms.assetid: 92b290a5-0923-42fc-8231-1decca26adc1
ms.date: 12/05/2018
ms.keywords: CoInstall, CoInstall function [Windows API], objbase/CoInstall, winprog.coinstall
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - CoInstall
 - objbase/CoInstall
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
 - CoInstall
---

# CoInstall function


## -description

<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future.]

Installs the requested COM server application.

## -parameters

### -param pbc [in]

Reserved for future use; this value must be <b>NULL</b>.

### -param dwFlags [in]

Reserved for future use; this value must be 0.

### -param pClassSpec [in]

A pointer to a <b>uCLSSPEC</b> union. The <b>tyspec</b> member must be set to TYSPEC_CLSID and the <b>clsid</b> member must be set to the CLSID to be installed. For more information, see <a href="/windows/desktop/DevNotes/tyspec">TYSPEC</a>.

### -param pQuery [in]

A pointer to a <a href="/previous-versions/bb432414(v=vs.85)">QUERYCONTEXT</a> structure. The <b>dwContext</b> field must be set to the desired <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> value. For more information, see <b>QUERYCONTEXT</b>.

### -param pszCodeBase [in]

Reserved for future use; this value must be <b>NULL</b>.

## -returns

This function supports the standard return value E_INVALIDARG, as well as the following.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="S_OK"></a><a id="s_ok"></a>S_OK

</td>
<td width="60%">
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<a id="CS_E_PACKAGE_NOTFOUND"></a><a id="cs_e_package_notfound"></a>CS_E_PACKAGE_NOTFOUND

</td>
<td width="60%">
The <b>tyspec</b> field of <i>pClassSpec</i> was not set to TYSPEC_CLSID.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/bb432414(v=vs.85)">QUERYCONTEXT</a>



<a href="/windows/desktop/DevNotes/tyspec">TYSPEC</a>