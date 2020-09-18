---
UID: NF:wdsbp.WdsBpInitialize
title: WdsBpInitialize function (wdsbp.h)
description: Constructs options for the WDS network boot program.
helpviewer_keywords: ["WDSBP_PK_TYPE_BCD","WDSBP_PK_TYPE_DHCPV6","WDSBP_PK_TYPE_WDSNBP","WdsBpInitialize","WdsBpInitialize function [Windows Deployment Services]","wds.wdsbpinitialize","wdsbp/WdsBpInitialize"]
old-location: wds\wdsbpinitialize.htm
tech.root: wds
ms.assetid: a77cbdf5-9025-4e98-8edd-1b9bae8493e7
ms.date: 12/05/2018
ms.keywords: WDSBP_PK_TYPE_BCD, WDSBP_PK_TYPE_DHCPV6, WDSBP_PK_TYPE_WDSNBP, WdsBpInitialize, WdsBpInitialize function [Windows Deployment Services], wds.wdsbpinitialize, wdsbp/WdsBpInitialize
req.header: wdsbp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.lib: Wdsbp.lib
req.dll: Wdsbp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsBpInitialize
 - wdsbp/WdsBpInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsbp.dll
api_name:
 - WdsBpInitialize
---

# WdsBpInitialize function


## -description

Constructs options for the WDS network boot program.

## -parameters

### -param bPacketType [in]

The type of boot program. This parameter may have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_WDSNBP"></a><a id="wdsbp_pk_type_wdsnbp"></a><dl>
<dt><b>WDSBP_PK_TYPE_WDSNBP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Specify this value to build a boot program using options for the "wdsnbp.com" boot program.  The "wdsnbp.com" boot program is the WDS network boot program for IPv4 PXE on legacy BIOS systems and does not support other systems.

</td>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_BCD"></a><a id="wdsbp_pk_type_bcd"></a><dl>
<dt><b>WDSBP_PK_TYPE_BCD</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Specify this value to build a boot program using the <b>WDSBP_OPT_BCD_FILE_PATH</b> option.  It may be used with "wdsnbp.com" or other boot programs.

</td>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_DHCPV6"></a><a id="wdsbp_pk_type_dhcpv6"></a><dl>
<dt><b>WDSBP_PK_TYPE_DHCPV6</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Specify this value to  indicate that the packet contains a path to a Boot Configuration Data (BCD) file. Use this value for any and all DHCPv6 options. The presence of this value indicates that the packet contains a path to a Boot Configuration Data (BCD) file. 

</td>
</tr>
</table>

### -param phHandle [out]

A pointer to the handle to the packet. This handle can be used by the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpaddoption">WdsBpAddOption</a> function to add options for the WDS network boot program. After all the options have been added, use the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpgetoptionbuffer">WdsBpGetOptionBuffer</a> function to add these to the DHCP options list sent to WDS network boot program. The handle must be closed using the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpclosehandle">WdsBpCloseHandle</a> function.

## -returns

If the function succeeds, the return is <b>S_OK</b>.