---
UID: NF:lmjoin.NetEnumerateComputerNames
title: NetEnumerateComputerNames function (lmjoin.h)
description: Enumerates names for the specified computer.
helpviewer_keywords: ["NetAllComputerNames","NetAlternateComputerNames","NetComputerNameTypeMax","NetEnumerateComputerNames","NetEnumerateComputerNames function [Network Management]","NetPrimaryComputerName","lmjoin/NetEnumerateComputerNames","netmgmt.netenumeratecomputernames"]
old-location: netmgmt\netenumeratecomputernames.htm
tech.root: NetMgmt
ms.assetid: c657ae33-404e-4c36-a956-5fbcfa540be7
ms.date: 12/05/2018
ms.keywords: NetAllComputerNames, NetAlternateComputerNames, NetComputerNameTypeMax, NetEnumerateComputerNames, NetEnumerateComputerNames function [Network Management], NetPrimaryComputerName, lmjoin/NetEnumerateComputerNames, netmgmt.netenumeratecomputernames
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
 - NetEnumerateComputerNames
 - lmjoin/NetEnumerateComputerNames
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
 - NetEnumerateComputerNames
---

# NetEnumerateComputerNames function


## -description

The
				<b>NetEnumerateComputerNames</b> function enumerates names for the specified computer.

## -parameters

### -param Server [in, optional]

A pointer to a constant string that specifies the name of the computer on which to execute this function. If this parameter is <b>NULL</b>, the local computer is used.

### -param NameType [in]

The type of the name queried. This member can be one of the following values defined in the <b>NET_COMPUTER_NAME_TYPE</b> enumeration defined in the <i>Lmjoin.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NetPrimaryComputerName"></a><a id="netprimarycomputername"></a><a id="NETPRIMARYCOMPUTERNAME"></a><dl>
<dt><b>NetPrimaryComputerName</b></dt>
</dl>
</td>
<td width="60%">
The primary computer name.

</td>
</tr>
<tr>
<td width="40%"><a id="NetAlternateComputerNames"></a><a id="netalternatecomputernames"></a><a id="NETALTERNATECOMPUTERNAMES"></a><dl>
<dt><b>NetAlternateComputerNames</b></dt>
</dl>
</td>
<td width="60%">
Alternate computer names.

</td>
</tr>
<tr>
<td width="40%"><a id="NetAllComputerNames"></a><a id="netallcomputernames"></a><a id="NETALLCOMPUTERNAMES"></a><dl>
<dt><b>NetAllComputerNames</b></dt>
</dl>
</td>
<td width="60%">
All computer names.

</td>
</tr>
<tr>
<td width="40%"><a id="NetComputerNameTypeMax"></a><a id="netcomputernametypemax"></a><a id="NETCOMPUTERNAMETYPEMAX"></a><dl>
<dt><b>NetComputerNameTypeMax</b></dt>
</dl>
</td>
<td width="60%">
Indicates the end of the range that specifies the possible values for the type of name to be queried.

</td>
</tr>
</table>

### -param Reserved [in]

Reserved for future use.   This parameter should be <b>NULL</b>.

### -param EntryCount [out]

A pointer to a DWORD value that returns the number of names returned
in the buffer pointed to by the <i>ComputerNames</i> parameter if the function succeeds.

### -param ComputerNames [out]

A pointer to an array of pointers to names.  If the function call is successful, this parameter will return the computer names that match the computer type name specified in the <i>NameType</i> parameter. 

When the application no longer needs this array, this buffer should be freed by
        calling <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. 

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

The <b>NetEnumerateComputerNames</b> function is supported on Windows Vista and later.  

The <b>NetEnumerateComputerNames</b> function is used to request the names a computer currently has configured. 

The <b>NetEnumerateComputerNames</b> function requires that the caller is a member of the Administrators local group on the target computer.

## -see-also

<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netaddalternatecomputername">NetAddAlternateComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netremovealternatecomputername">NetRemoveAlternateComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netrenamemachineindomain">NetRenameMachineInDomain</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netsetprimarycomputername">NetSetPrimaryComputerName</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netunjoindomain">NetUnjoinDomain</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a>