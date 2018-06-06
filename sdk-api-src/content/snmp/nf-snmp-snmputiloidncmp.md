---
UID: NF:snmp.SnmpUtilOidNCmp
title: SnmpUtilOidNCmp function
author: windows-sdk-content
description: The SnmpUtilOidNCmp function compares two object identifiers.
old-location: snmp\snmputiloidncmp.htm
old-project: SNMP
ms.assetid: a23df516-9559-4209-bf2d-8268737d1dfb
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SnmpUtilOidNCmp, SnmpUtilOidNCmp function [SNMP], _snmp_snmputiloidncmp, snmp.snmputiloidncmp, snmp/SnmpUtilOidNCmp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: snmp.h
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
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilOidNCmp
product: Windows
targetos: Windows
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpUtilOidNCmp function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidNCmp</b> function compares two object identifiers. The function compares the subidentifiers in the variables until it reaches the number of subidentifiers specified by the <i>nSubIds</i> parameter. 
<b>SnmpUtilOidNCmp</b> is an element of the SNMP Utility API.


## -parameters




### -param pOid1 [in]

Pointer to an 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to compare.


### -param pOid2 [in]

Pointer to a second 
<a href="https://msdn.microsoft.com/695e5581-00df-49af-8abe-1dd1b25cb215">AsnObjectIdentifier</a> structure to compare.


### -param nSubIds [in]

Specifies the number of subidentifiers to compare.


## -returns



The function returns a value greater than zero if <i>pOid1</i> is greater than <i>pOid2</i>, zero if <i>pOid1</i> equals <i>pOid2</i>, and less than zero if <i>pOid1</i> is less than <i>pOid2</i>.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/c6ec4984-d984-4642-b110-fd9c2c7e3c5d">SnmpUtilOidCmp</a>
 

 

