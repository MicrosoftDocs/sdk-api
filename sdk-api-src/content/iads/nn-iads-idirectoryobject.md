---
UID: NN:iads.IDirectoryObject
title: IDirectoryObject
author: windows-sdk-content
description: The IDirectoryObject interface is a non-Automation COM interface that provides clients with direct access to directory service objects.
old-location: adsi\idirectoryobject.htm
old-project: ADSI
ms.assetid: bc4f8920-2881-4393-bb01-ed837c3db6ad
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDirectoryObject, IDirectoryObject interface [ADSI], IDirectoryObject interface [ADSI],described, _ds_idirectoryobject_ref, adsi.idirectoryobject, adsi.idirectoryobject__ref, iads/IDirectoryObject
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IDirectoryObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDirectoryObject interface


## -description


The <b>IDirectoryObject</b> interface is a non-Automation COM interface that provides clients with direct access to directory service objects. The interface enables access by means of a direct over-the-wire protocol, rather than through the ADSI attribute cache. Using the over-the-wire protocol optimizes performance. With <b>IDirectoryObject</b>, a client can get, or set, any number of object attributes with one method call. Unlike the corresponding Automation methods, which are invoked in batch, those of <b>IDirectoryObject</b> are executed when they are called. <b>IDirectoryObject</b> performs no attribute caching.
   

Non-Automation clients can call the methods of <b>IDirectoryObject</b> to optimize performance and take advantage of native directory service interfaces. Automation clients cannot use <b>IDirectoryObject</b>. Instead, they should use the  <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface.

Of the ADSI system-supplied providers, only the LDAP provider supports this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectoryObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectoryObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectoryObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77648d1c-b05b-4c36-a2e3-25bb5713d615">CreateDSObject</a>
</td>
<td align="left" width="63%">
Creates a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb7bed74-1420-4b46-92a9-ebe31f2d88fd">DeleteDSObject</a>
</td>
<td align="left" width="63%">
Deletes a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e3d046f-eac0-4955-925b-71ab15df9ed3">GetObjectAttributes</a>
</td>
<td align="left" width="63%">
Gets one or more attributes of a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a2d7fee-666e-4b3b-b6fa-b9f6d785c2c1">GetObjectInformation</a>
</td>
<td align="left" width="63%">
Gets data about a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/999e6766-52cf-4087-bb17-72de487975c2">SetObjectAttributes</a>
</td>
<td align="left" width="63%">
Sets one or more attributes of a directory service object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>
 

 

