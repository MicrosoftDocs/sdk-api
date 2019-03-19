---
UID: NN:certenroll.IX509MachineEnrollmentFactory
title: IX509MachineEnrollmentFactory (certenroll.h)
author: windows-sdk-content
description: Can be used to create an IX509EnrollmentHelper object on a webpage.
old-location: security\ix509machineenrollmentfactory.htm
tech.root: seccertenroll
ms.assetid: 2f97fdd7-13ca-4427-8ec5-24302d245fdb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509MachineEnrollmentFactory, IX509MachineEnrollmentFactory interface [Security], IX509MachineEnrollmentFactory interface [Security],described, certenroll/IX509MachineEnrollmentFactory, security.ix509machineenrollmentfactory
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: CertEnroll.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509MachineEnrollmentFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509MachineEnrollmentFactory interface


## -description


The <b>IX509MachineEnrollmentFactory</b> interface can be used to create an <a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a> object on a webpage. This object cannot be created directly inside of a script.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509MachineEnrollmentFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509MachineEnrollmentFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IX509MachineEnrollmentFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9a45219-1c88-4946-ad57-81b95c609066">CreateObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/19124591-be1a-401e-9b83-c640d00de34a">IX509EnrollmentHelper</a> object on a webpage.

[WebEnabled]

</td>
</tr>
</table> 

