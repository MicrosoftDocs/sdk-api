---
UID: NS:ocidl.tagCONNECTDATA
title: tagCONNECTDATA
author: windows-sdk-content
description: Describes a connection that exists to a given connection point.
old-location: com\connectdata.htm
tech.root: com
ms.assetid: 23312f89-2985-402d-aae4-cd7388137153
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPCONNECTDATA, *PCONNECTDATA, CONNECTDATA, CONNECTDATA structure [COM], LPCONNECTDATA, LPCONNECTDATA structure pointer [COM], PCONNECTDATA, PCONNECTDATA structure pointer [COM], _com_CONNECTDATA, com.connectdata, ocidl/CONNECTDATA, ocidl/LPCONNECTDATA, ocidl/PCONNECTDATA, tagCONNECTDATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ocidl.h
api_name:
 - CONNECTDATA
product: Windows
targetos: Windows
req.typenames: CONNECTDATA, *PCONNECTDATA, *LPCONNECTDATA
req.redist: 
---

# tagCONNECTDATA structure


## -description


Describes a connection that exists to a given connection point.



## -struct-fields




### -field pUnk

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on a connected advisory sink. The caller must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> using this pointer when the <b>CONNECTDATA</b> structure is no longer needed. The caller is responsible for calling <b>Release</b> for each <b>CONNECTDATA</b> structure enumerated through <a href="https://msdn.microsoft.com/af58f961-1182-43fc-95ce-4afb251b9b08">IEnumConnections::Next</a>.


### -field dwCookie

Connection where this value is the same token that is returned originally from calls to <a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">IConnectionPoint::Advise</a>. This token can be used to disconnect the sink pointed to by a <b>pUnk</b> by passing <b>dwCookie</b> to <a href="https://msdn.microsoft.com/71641bad-2fd1-4d94-a6d0-116f5687a95b">IConnectionPoint::Unadvise</a>.



## -see-also




<a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>



<a href="https://msdn.microsoft.com/464966c1-e4e9-4b58-9e41-48de408f572f">IEnumConnections</a>
 

 

