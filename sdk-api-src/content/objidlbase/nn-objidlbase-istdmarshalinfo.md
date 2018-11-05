---
UID: NN:objidlbase.IStdMarshalInfo
title: IStdMarshalInfo
author: windows-sdk-content
description: Retrieves the CLSID identifying the handler to be used in the destination process during standard marshaling.
old-location: com\istdmarshalinfo.htm
tech.root: com
ms.assetid: f034436f-e24e-4b99-9fb9-b0400d3ebb72
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IStdMarshalInfo, IStdMarshalInfo interface [COM], IStdMarshalInfo interface [COM],described, _com_istdmarshalinfo, com.istdmarshalinfo, objidlbase/IStdMarshalInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IStdMarshalInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStdMarshalInfo interface


## -description


Retrieves the CLSID identifying the handler to be used in the destination process during standard marshaling.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStdMarshalInfo</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IStdMarshalInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStdMarshalInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab68f292-851d-4908-b545-4df2931fceae">GetClassForHandler</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the object handler to be used in the destination process during standard marshaling.

</td>
</tr>
</table> 


## -remarks



An object that uses OLE's default implementation of <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> does not provide its own proxy but, by implementing <b>IStdMarshalInfo</b>, can nevertheless specify a handler to be loaded in the client process. Such a handler would typically handle certain requests in-process and use OLE's default marshaling to delegate others back to the original object.

To create an instance of an object in some client process, COM must first determine whether the object uses default marshaling or its own implementation. If the object uses default marshaling, COM then queries the object to determine whether it uses a special handler or, simply, OLE's default proxy. To get the CLSID of the handler to be loaded, COM queries the object for <b>IStdMarshalInfo</b> and then the <a href="https://msdn.microsoft.com/932eb0e2-35a6-482e-9138-00cff30508a9">IPersist</a> interface. If neither interface is supported, a standard handler is used.




## -see-also




<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>
 

 

