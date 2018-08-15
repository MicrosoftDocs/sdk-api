---
UID: NF:mgmtapi.SnmpMgrStrToOid
title: SnmpMgrStrToOid function
author: windows-sdk-content
description: The SnmpMgrStrToOid function converts the string format of an object identifier to its internal object identifier structure. This function is an element of the SNMP Management API.
old-location: snmp\snmpmgrstrtooid.htm
old-project: snmp
ms.assetid: d245b43c-3893-4081-874c-93619a8c461c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SnmpMgrStrToOid, SnmpMgrStrToOid function [SNMP], _snmp_snmpmgrstrtooid, mgmtapi/SnmpMgrStrToOid, snmp.snmpmgrstrtooid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mgmtapi.h
req.include-header: 
req.redist: 
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
 - SnmpMgrStrToOid
product: Windows
targetos: Windows
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SnmpMgrStrToOid function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrStrToOid</b> function converts the string format of an object identifier to its internal object identifier structure. This function is an element of the SNMP Management API.


## -parameters




### -param string [in]

Pointer to a null-terminated string to convert.


### -param oid [out]

Pointer to an object identifier variable to receive the converted value.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If the function succeeds, call the 
<a href="https://msdn.microsoft.com/8fc44fdf-956a-4102-bcbb-4cd17a73828c">SnmpUtilOidFree</a> function to free the memory allocated for the converted object identifier.

If an application passes a valid object identifier to 
<b>SnmpMgrStrToOid</b>, yet is unable to obtain the requested variable, then the syntax of the system group and object identifier is incorrect. This occurs because 
<b>SnmpMgrStrToOid</b> assumes that the object identifier is under the Internet MIB of the management subtree.

You must always precede the object identifier with a period (.) to obtain the correct system group (for example, ".1.3.6.1.2.1.1"). If an application passes the variable "1.3.6.1.2.1.1", 
<b>SnmpMgrStrToOid</b> cannot interpret the object identifier correctly.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/4864b864-3381-4129-8cc3-ecfc6566e530">SnmpMgrOidToStr</a>



<a href="https://msdn.microsoft.com/8fc44fdf-956a-4102-bcbb-4cd17a73828c">SnmpUtilOidFree</a>
 

 

