---
UID: NN:restrictederrorinfo.ILanguageExceptionTransform
title: ILanguageExceptionTransform
author: windows-driver-content
description: Allows language projections to make available to the system any and all context from an exception that gets thrown from the context of a catch handler that catches a different exception.
old-location: winrt\ilanguageexceptiontransform.htm
old-project: WinRT
ms.assetid: A42470EE-FA05-4716-BA17-009D59FEE259
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ILanguageExceptionTransform, ILanguageExceptionTransform interface [Windows Runtime], ILanguageExceptionTransform interface [Windows Runtime],described, restrictederrorinfo/ILanguageExceptionTransform, winrt.ilanguageexceptiontransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Restrictederrorinfo.idl
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
-	restrictederrorinfo.h
api_name:
-	ILanguageExceptionTransform
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ILanguageExceptionTransform interface


## -description


Allows language projections to make available to the system any and all context from an exception that gets thrown from the context of a catch handler that catches a different exception. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageExceptionTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILanguageExceptionTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageExceptionTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F64449FE-9562-4210-8C00-9935DE71DA07">GetTransformedRestrictedErrorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the transformed restricted error info.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

