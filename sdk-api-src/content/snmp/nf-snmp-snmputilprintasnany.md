---
UID: NF:snmp.SnmpUtilPrintAsnAny
title: SnmpUtilPrintAsnAny function
author: windows-sdk-content
description: The SnmpUtilPrintAsnAny function prints the value of the Any parameter to the standard output. This function is an element of the SNMP Utility API.
old-location: snmp\snmputilprintasnany.htm
old-project: snmp
ms.assetid: 2dd52131-defb-4613-a889-a115d60a969a
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: SnmpUtilPrintAsnAny, SnmpUtilPrintAsnAny function [SNMP], _snmp_snmputilprintasnany, snmp.snmputilprintasnany, snmp/SnmpUtilPrintAsnAny
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
 - SnmpUtilPrintAsnAny
product: Windows
targetos: Windows
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SnmpUtilPrintAsnAny function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilPrintAsnAny</b> function prints the value of the <i>Any</i> parameter to the standard output. This function is an element of the SNMP Utility API.


## -parameters




### -param pAny [in]

Pointer to an 
<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a> structure for a value to print.


## -returns



This function does not return a value.




## -remarks



Use the 
<b>SnmpUtilPrintAsnAny</b> function for debugging and development purposes. This function does not generally print the data in a form that a manager application would typically need.




## -see-also




<a href="https://msdn.microsoft.com/ce8d002e-f357-499c-b976-f8ebaf1e7142">AsnAny</a>



<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>
 

 

