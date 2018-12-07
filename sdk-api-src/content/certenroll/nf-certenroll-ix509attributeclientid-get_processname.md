---
UID: NF:certenroll.IX509AttributeClientId.get_ProcessName
title: IX509AttributeClientId::get_ProcessName
author: windows-sdk-content
description: Retrieves the name of the application that generated the request.
old-location: security\ix509attributeclientid_processname_property.htm
tech.root: seccertenroll
ms.assetid: 7e273ffe-3f80-49b6-a4e5-939f5ba9d5bd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509AttributeClientId interface [Security],ProcessName property, IX509AttributeClientId.ProcessName, IX509AttributeClientId.get_ProcessName, IX509AttributeClientId::ProcessName, IX509AttributeClientId::get_ProcessName, ProcessName property [Security], ProcessName property [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::ProcessName, certenroll/IX509AttributeClientId::get_ProcessName, get_ProcessName, security.ix509attributeclientid_processname_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeClientId.ProcessName
 - IX509AttributeClientId.get_ProcessName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeClientId::get_ProcessName


## -description


The <b>ProcessName</b> property retrieves the name of the application that generated the request.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377076(v=VS.85).aspx">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/en-us/library/Aa377075(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>ProcessName</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377074(v=VS.85).aspx">ClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377077(v=VS.85).aspx">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377081(v=VS.85).aspx">UserSamName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

