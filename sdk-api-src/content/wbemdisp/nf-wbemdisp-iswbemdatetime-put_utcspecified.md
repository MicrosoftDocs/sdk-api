---
UID: NF:wbemdisp.ISWbemDateTime.put_UTCSpecified
title: ISWbemDateTime::put_UTCSpecified
author: windows-sdk-content
description: Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.
old-location: wmi\swbemdatetime_utcspecified.htm
old-project: WmiSdk
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemDateTime interface [Windows Management Instrumentation],UTCSpecified property, ISWbemDateTime.get_UTCSpecified, ISWbemDateTime.put_UTCSpecified, ISWbemDateTime::put_UTCSpecified, SWbemDateTime object [Windows Management Instrumentation],UTCSpecified property, SWbemDateTime.UTCSpecified, UTCSpecified property [Windows Management Instrumentation], UTCSpecified property [Windows Management Instrumentation],ISWbemDateTime interface, UTCSpecified property [Windows Management Instrumentation],SWbemDateTime object, _hmm_swbemdatetime.utcspecified, put_UTCSpecified, wmi.swbemdatetime_utcspecified
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemDateTime.UTCSpecified
 - ISWbemDateTime.UTCSpecified
 - ISWbemDateTime.get_UTCSpecified
 - ISWbemDateTime.put_UTCSpecified
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime::put_UTCSpecified


## -description


The 
<b>UTCSpecified</b> property of the 
<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a> object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value. If 
<b>UTCSpecified</b> is <b>TRUE</b> and 
<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is <b>FALSE</b>, then 
<a href="https://msdn.microsoft.com/43d9d0c8-5521-410f-825b-6b00c3dd0039">SWbemDateTime.UTC</a> contains a <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> value. A <b>DATETIME</b> value that contains an interval cannot be converted into either the <b>VT_DATE</b> format or the <b>FILETIME</b> format. If 
<b>UTCSpecified</b> is <b>FALSE</b> and 
<b>IsInterval</b> is <b>TRUE</b>, then <b>SWbemDateTime.UTC</b> contains an interval.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/3dd34c73-3c2b-4d59-827b-169cf8020213">SWbemDateTime</a>



<a href="https://msdn.microsoft.com/43d9d0c8-5521-410f-825b-6b00c3dd0039">SWbemDateTime.UTC</a>
 

 

