---
UID: NF:lmjoin.NetRemoveAlternateComputerName
title: NetRemoveAlternateComputerName function (lmjoin.h)
description: Removes an alternate name for the specified computer.
helpviewer_keywords: ["NetRemoveAlternateComputerName","NetRemoveAlternateComputerName function [Network Management]","lmjoin/NetRemoveAlternateComputerName","netmgmt.netremovealternatecomputername"]
old-location: netmgmt\netremovealternatecomputername.htm
tech.root: NetMgmt
ms.assetid: 3c7ab44e-d5fa-40da-83fe-a44bf85b2ba5
ms.date: 12/05/2018
ms.keywords: NetRemoveAlternateComputerName, NetRemoveAlternateComputerName function [Network Management], lmjoin/NetRemoveAlternateComputerName, netmgmt.netremovealternatecomputername
req.header: lmjoin.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetRemoveAlternateComputerName
 - lmjoin/NetRemoveAlternateComputerName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetRemoveAlternateComputerName
---

# NetRemoveAlternateComputerName function


## -description

The
				<b>NetRemoveAlternateComputerName</b> function removes an alternate name for the specified computer.

## -parameters

### -param Server [in, optional]

A pointer to a constant string that specifies the name of the computer on which to execute this function. If this parameter is <b>NULL</b>, the local computer is used.

### -param AlternateName [in]

A pointer to a constant string that specifies the alternate name to remove. This name must be in the form of a fully qualified DNS name.

### -param DomainAccount [in, optional]

A pointer to a constant string that specifies the domain account to use for accessing the
        machine account object for the computer specified in the <i>Server</i> parameter in Active Directory. If this parameter is <b>NULL</b>, then the credentials of the user executing
        this routine are used. 

This parameter is not used if the server to execute this function is not joined to a domain.

### -param DomainAccountPassword [in, optional]

A pointer to a constant string that specifies the password matching the domain account passed in the <i>DomainAccount</i> parameter.
        If this parameter is <b>NULL</b>, then the credentials of the user executing
        this routine are used. 

This parameter is ignored if the <i>DomainAccount</i> parameter is <b>NULL</b>. This parameter is not used if the server to execute this function is not joined to a domain.

### -param Reserved [in]

Reserved for future use.   This parameter should be <b>NULL</b>.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes or one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned if the caller was not a member of the Administrators local group on the target computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
A name parameter is incorrect. This error is returned if the <i>AlternateName</i> parameter does not contain valid name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if the <i>DomainAccount</i> parameter does not contain a valid domain. This error is also returned if the <i>DomainAccount</i> parameter is not <b>NULL</b> and the <i>DomainAccountPassword</i> parameter is not <b>NULL</b> but does not contain a Unicode string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to process this command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if the target computer specified in the <i>Server</i> parameter on which this function executes is running on Windows 2000 and earlier. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_WkstaNotStarted</b></dt>
</dl>
</td>
<td width="60%">
The Workstation service has not been started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALL_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A remote procedure call is already in progress for this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_PROTSEQ_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The remote procedure call protocol sequence is not supported.

</td>
</tr>
</table>

## -remarks

The <b>NetRemoveAlternateComputerName</b> function is supported on Windows XP and later.  

The <b>NetRemoveAlternateComputerName</b> function is used to remove secondary computer names configured for the target computer.

The <b>NetRemoveAlternateComputerName</b> function requires that the caller is a member of the Administrators local group on the target computer.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netaddalternatecomputername">NetAddAlternateComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netenumeratecomputernames">NetEnumerateComputerNames</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netsetprimarycomputername">NetSetPrimaryComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a>