---
UID: NN:restrictederrorinfo.IRestrictedErrorInfo
title: IRestrictedErrorInfo
author: windows-driver-content
description: Represents the details of an error, including restricted error information.
old-location: winrt\irestrictederrorinfo.htm
old-project: WinRT
ms.assetid: 1af8d4bf-1217-44ca-b0dd-9a6feda16100
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: IRestrictedErrorInfo, IRestrictedErrorInfo interface [Windows Runtime], IRestrictedErrorInfo interface [Windows Runtime],described, restrictederrorinfo/IRestrictedErrorInfo, winrt.irestrictederrorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RestrictedErrorInfo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RestrictedErrorInfo.h
api_name:
-	IRestrictedErrorInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRestrictedErrorInfo interface


## -description


Represents the details of an error, including restricted error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRestrictedErrorInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRestrictedErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRestrictedErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecfd97cf-9f8f-4940-9499-a894e0883f04">GetErrorDetails</a>
</td>
<td align="left" width="63%">
Returns information about an error, including the restricted error description.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7f0c451-c6a4-49ec-a97a-dc834081b3c1">GetReference</a>
</td>
<td align="left" width="63%">
Returns a reference to restricted error information. 

</td>
</tr>
</table> 

