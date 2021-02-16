---
UID: NF:bits3_0.IBitsPeerCacheAdministration.GetConfigurationFlags
title: IBitsPeerCacheAdministration::GetConfigurationFlags (bits3_0.h)
description: Gets the configuration flags that determine if the computer serves content to peers and can download content from peers.
helpviewer_keywords: ["BG_ENABLE_PEERCACHING_CLIENT","BG_ENABLE_PEERCACHING_SERVER","GetConfigurationFlags","GetConfigurationFlags method [BITS]","GetConfigurationFlags method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","GetConfigurationFlags method","IBitsPeerCacheAdministration.GetConfigurationFlags","IBitsPeerCacheAdministration::GetConfigurationFlags","bits.ibitspeercacheadministration_getconfigurationflags","bits3_0/IBitsPeerCacheAdministration::GetConfigurationFlags"]
old-location: bits\ibitspeercacheadministration_getconfigurationflags.htm
tech.root: Bits
ms.assetid: caa54ee0-c771-47e7-95d1-26a812f0f95f
ms.date: 12/05/2018
ms.keywords: BG_ENABLE_PEERCACHING_CLIENT, BG_ENABLE_PEERCACHING_SERVER, GetConfigurationFlags, GetConfigurationFlags method [BITS], GetConfigurationFlags method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],GetConfigurationFlags method, IBitsPeerCacheAdministration.GetConfigurationFlags, IBitsPeerCacheAdministration::GetConfigurationFlags, bits.ibitspeercacheadministration_getconfigurationflags, bits3_0/IBitsPeerCacheAdministration::GetConfigurationFlags
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBitsPeerCacheAdministration::GetConfigurationFlags
 - bits3_0/IBitsPeerCacheAdministration::GetConfigurationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheAdministration.GetConfigurationFlags
---

# IBitsPeerCacheAdministration::GetConfigurationFlags


## -description

Gets the configuration flags that determine if the computer serves content to peers and can download content from peers.

## -parameters

### -param pFlags [out]

Flags that determine if the computer serves content to peers and can download content from peers. The following flags can be set:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_ENABLE_PEERCACHING_CLIENT"></a><a id="bg_enable_peercaching_client"></a><dl>
<dt><b>BG_ENABLE_PEERCACHING_CLIENT</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The computer can download content from peers.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_ENABLE_PEERCACHING_SERVER"></a><a id="bg_enable_peercaching_server"></a><dl>
<dt><b>BG_ENABLE_PEERCACHING_SERVER</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The computer can serve content to peers.

</td>
</tr>
</table>

## -returns

The method returns the following return values.

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
Success

</td>
</tr>
</table>

## -remarks

BITS can download from peers only if peercaching is enabled both at the computer level and at the job level; this API affects only the computer level. For details, see <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags">IBitsPeerCacheAdministration::SetConfigurationFlags</a>.

Peer caching could have been enabled by Group Policy or by calling the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags">IBitsPeerCacheAdministration::SetConfigurationFlags</a> method.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags">IBitsPeerCacheAdministration::SetConfigurationFlags</a>