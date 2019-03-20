---
UID: NF:mgmtapi.SnmpMgrOidToStr
title: SnmpMgrOidToStr function (mgmtapi.h)
author: windows-sdk-content
description: The SnmpMgrOidToStr function converts an internal object identifier structure to its string representation. This function is an element of the SNMP Management API.
old-location: snmp\snmpmgroidtostr.htm
tech.root: SNMP
ms.assetid: 4864b864-3381-4129-8cc3-ecfc6566e530
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpMgrOidToStr, SnmpMgrOidToStr function [SNMP], _snmp_snmpmgroidtostr, mgmtapi/SnmpMgrOidToStr, snmp.snmpmgroidtostr
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
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mgmtapi.dll
api_name:
 - SnmpMgrOidToStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpMgrOidToStr function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrOidToStr</b> function converts an internal object identifier structure to its string representation. This function is an element of the SNMP Management API.


## -parameters




### -param oid [in]

Pointer to an object identifier variable to convert.


### -param string [out]

Pointer to a null-terminated string to receive the converted value.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If the function succeeds, call the 
<a href="https://msdn.microsoft.com/57cf0398-d2c1-4dd9-ad77-0c453412034a">SnmpUtilMemFree</a> function to free the memory allocated for the converted string.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/d245b43c-3893-4081-874c-93619a8c461c">SnmpMgrStrToOid</a>



<a href="https://msdn.microsoft.com/57cf0398-d2c1-4dd9-ad77-0c453412034a">SnmpUtilMemFree</a>
 

 

