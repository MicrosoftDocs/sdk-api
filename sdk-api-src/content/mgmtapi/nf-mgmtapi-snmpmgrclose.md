---
UID: NF:mgmtapi.SnmpMgrClose
title: SnmpMgrClose function (mgmtapi.h)
description: The SnmpMgrClose function closes the communications sockets and data structures that are associated with the specified session. This function is an element of the SNMP Management API.
helpviewer_keywords: ["SnmpMgrClose","SnmpMgrClose function [SNMP]","_snmp_snmpmgrclose","mgmtapi/SnmpMgrClose","snmp.snmpmgrclose"]
old-location: snmp\snmpmgrclose.htm
tech.root: SNMP
ms.assetid: d8e7cc61-e313-4e36-88e7-686b4f9282b5
ms.date: 12/05/2018
ms.keywords: SnmpMgrClose, SnmpMgrClose function [SNMP], _snmp_snmpmgrclose, mgmtapi/SnmpMgrClose, snmp.snmpmgrclose
req.header: mgmtapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpMgrClose
 - mgmtapi/SnmpMgrClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mgmtapi.dll
api_name:
 - SnmpMgrClose
---

# SnmpMgrClose function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrClose</b> function closes the communications sockets and data structures that are associated with the specified session. This function is an element of the SNMP Management API.

## -parameters

### -param session [in]

Pointer to an internal structure that specifies the session to close. For more information, see the following Remarks section.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

 This function may return Windows Sockets error codes.

## -remarks

<b>Windows Server 2003:  </b>SNMP manager applications can call 
<b>SnmpMgrClose</b> with a <b>NULL</b><i>session</i> parameter to clean up the resources that are associated with a successful call to the 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrtraplisten">SnmpMgrTrapListen</a> function. Note, however, that if your application is a DLL, it should not call 
<b>SnmpMgrClose</b> from its 
<a href="/windows/desktop/Dlls/dllmain">DllMain</a> entry-point function.<p class="note"><b>SnmpMgrClose</b> must not be called when the application DLL is in the process of unloading.



<b>Windows Server 2003:  </b><b>SnmpMgrClose</b> takes longer to execute under  Windows Server 2003 when compared to an identical call under Windows 2000. Specifically, a call to this API takes up to a second to execute under Windows Server 2003, whereas the same call takes around .3 milliseconds under Windows 2000. this may cause performance problems for Windows Server 2003 SNMP applications that call  <a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgropen">SnmpMgrOpen</a> and <b>SnmpMgrClose</b> frequently.

<p class="note">To address this problem,  create an extra SNMP manager session by calling <a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgropen">SnmpMgrOpen</a> on the local host during application startup, and keep it open for the duration of the application's lifetime. Closing the session manager will close all associated sessions, requiring only one call to <b>SnmpMgrClose</b>.



<b>Windows Server 2003 with SP1:  </b>The above issue does not apply to Windows 2003 Service Pack 1.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgropen">SnmpMgrOpen</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrrequest">SnmpMgrRequest</a>