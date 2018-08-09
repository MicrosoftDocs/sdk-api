---
UID: NF:mgmtapi.SnmpMgrClose
title: SnmpMgrClose function
author: windows-sdk-content
description: The SnmpMgrClose function closes the communications sockets and data structures that are associated with the specified session. This function is an element of the SNMP Management API.
old-location: snmp\snmpmgrclose.htm
old-project: snmp
ms.assetid: d8e7cc61-e313-4e36-88e7-686b4f9282b5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SnmpMgrClose, SnmpMgrClose function [SNMP], _snmp_snmpmgrclose, mgmtapi/SnmpMgrClose, snmp.snmpmgrclose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: SOURCE_GROUP_ENTRY, *PSOURCE_GROUP_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mgmtapi.dll
api_name:
 - SnmpMgrClose
product: Windows
targetos: Windows
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SnmpMgrClose function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

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
<a href="https://msdn.microsoft.com/9ba799a7-0088-4939-9665-ce96074c6448">SnmpMgrTrapListen</a> function. Note, however, that if your application is a DLL, it should not call 
<b>SnmpMgrClose</b> from its 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> entry-point function.<p class="note"><b>SnmpMgrClose</b> must not be called when the application DLL is in the process of unloading.



<b>Windows Server 2003:  </b><b>SnmpMgrClose</b> takes longer to execute under  Windows Server 2003 when compared to an identical call under Windows 2000. Specifically, a call to this API takes up to a second to execute under Windows Server 2003, whereas the same call takes around .3 milliseconds under Windows 2000. this may cause performance problems for Windows Server 2003 SNMP applications that call  <a href="https://msdn.microsoft.com/e2827352-f1aa-477e-933c-942c73cea487">SnmpMgrOpen</a> and <b>SnmpMgrClose</b> frequently.

<p class="note">To address this problem,  create an extra SNMP manager session by calling <a href="https://msdn.microsoft.com/e2827352-f1aa-477e-933c-942c73cea487">SnmpMgrOpen</a> on the local host during application startup, and keep it open for the duration of the application's lifetime. Closing the session manager will close all associated sessions, requiring only one call to <b>SnmpMgrClose</b>.



<b>Windows Server 2003 with SP1:  </b>The above issue does not apply to Windows 2003 Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/e2827352-f1aa-477e-933c-942c73cea487">SnmpMgrOpen</a>



<a href="https://msdn.microsoft.com/f66ce774-dba0-466b-ad1e-671f9a487e0f">SnmpMgrRequest</a>
 

 

