---
UID: NF:ntsecapi.LsaGetLogonSessionData
title: LsaGetLogonSessionData function (ntsecapi.h)
description: Retrieves information about a specified logon session.
helpviewer_keywords: ["LsaGetLogonSessionData","LsaGetLogonSessionData function [Security]","_lsa_lsagetlogonsessiondata","ntsecapi/LsaGetLogonSessionData","security.lsagetlogonsessiondata"]
old-location: security\lsagetlogonsessiondata.htm
tech.root: security
ms.assetid: b1478a7a-f508-4b98-8c7b-adeb2f07bb86
ms.date: 12/05/2018
ms.keywords: LsaGetLogonSessionData, LsaGetLogonSessionData function [Security], _lsa_lsagetlogonsessiondata, ntsecapi/LsaGetLogonSessionData, security.lsagetlogonsessiondata
req.header: ntsecapi.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaGetLogonSessionData
 - ntsecapi/LsaGetLogonSessionData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaGetLogonSessionData
---

# LsaGetLogonSessionData function


## -description

The <b>LsaGetLogonSessionData</b> function retrieves information about a specified logon session.

To retrieve information about a logon session, the caller must be the owner of the session or a local system administrator.

## -parameters

### -param LogonId [in]

Specifies a pointer to a <b>LUID</b> that identifies the logon session whose information will be retrieved. For information about valid values for this parameter, see Remarks.

### -param ppLogonSessionData [out]

Address of a pointer to a 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-security_logon_session_data">SECURITY_LOGON_SESSION_DATA</a> structure containing information on the logon session specified by <i>LogonId</i>. This structure is allocated by the LSA. When the information is no longer needed, call the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreereturnbuffer">LsaFreeReturnBuffer</a> function to free the memory used by this structure.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an <b>NTSTATUS</b> code indicating the reason.

## -remarks

To obtain valid logon session identifiers that may be passed to this function's <i>LogonId</i> parameter, call the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratelogonsessions">LsaEnumerateLogonSessions</a> function.

If  <i>LogonID</i> specifies the LocalSystem account (0x0:0x3e7), then this function returns zero for the logon session data retrieved in <i>ppLogonSessionData</i>. The reason is that the LocalSystem account does not get logged on in the typical logon manner. Rather, the LocalSystem account is active after the system starts.