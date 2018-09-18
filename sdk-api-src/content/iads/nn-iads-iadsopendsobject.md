---
UID: NN:iads.IADsOpenDSObject
title: IADsOpenDSObject
author: windows-sdk-content
description: The IADsOpenDSObject interface is designed to supply a security context for binding to an object in the underlying directory store.
old-location: adsi\iadsopendsobject.htm
tech.root: ADSI
ms.assetid: 9daf6f91-6c58-46a8-ba05-149f28b53829
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsOpenDSObject, IADsOpenDSObject interface [ADSI], IADsOpenDSObject interface [ADSI],described, _ds_iadsopendsobject, adsi.iadsopendsobject, iads/IADsOpenDSObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iads.h
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
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsOpenDSObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsOpenDSObject interface


## -description


The <b>IADsOpenDSObject</b> interface is designed to supply a security context for binding to an object in the underlying directory store. It provides a means for specifying credentials of a client. Use this interface to bind to an ADSI object when you must supply a set of credentials for authentication in any directory service.

ADSI maintains the security context in its cache. Thus, throughout the connection within a process, Once authenticated, the supplied user credentials are applied to any actions performed on this object and its children. This credential caching model applies to binding to different objects as well, provided that the binding takes place within the same connection and process.

Calling the <a href="https://msdn.microsoft.com/9984ddb4-58bb-4264-930b-07e6534dc69f">OpenDSObject</a> method of this interface yields the cache handle. Releasing this cache handle releases the security context as well.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsOpenDSObject</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IADsOpenDSObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsOpenDSObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9984ddb4-58bb-4264-930b-07e6534dc69f">OpenDSObject</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface on the specified object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/690b0c96-6319-42d8-8b0e-c43f46f91031">IADsClass</a>



<a href="https://msdn.microsoft.com/9984ddb4-58bb-4264-930b-07e6534dc69f">IADsOpenDSObject::OpenDSObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

