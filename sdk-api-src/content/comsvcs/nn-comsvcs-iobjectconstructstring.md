---
UID: NN:comsvcs.IObjectConstructString
title: IObjectConstructString
author: windows-sdk-content
description: Provides access to a constructor string. Use it when you want to specify the parameters during the construction of your object.
old-location: cos\iobjectconstructstring.htm
old-project: cossdk
ms.assetid: ebfa8384-1efd-4775-b66f-b8048af33abc
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IObjectConstructString, IObjectConstructString interface [COM+], IObjectConstructString interface [COM+],described, _cos_IObjectConstructString, comsvcs/IObjectConstructString, cos.iobjectconstructstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectConstructString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IObjectConstructString interface


## -description


Provides access to a constructor string. Use it when you want to specify the parameters during the construction of your object.

Object constructor strings should not be used to store security-sensitive information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectConstructString</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IObjectConstructString</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectConstructString</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/154b7567-0f25-49c3-90b2-58c95f0ebfee">get_ConstructString</a>
</td>
<td align="left" width="63%">
Retrieves the constructor string for the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5e630812-b2cf-4512-af67-6e919a02bf95">COM+ Object Constructor Strings</a>



<a href="https://msdn.microsoft.com/ebfa8384-1efd-4775-b66f-b8048af33abc">IObjectConstructString</a>



<a href="https://msdn.microsoft.com/0c5aaaae-368e-4b3e-a483-b3a23c353e6e">Specifying an Object Constructor String for a Component</a>
 

 

