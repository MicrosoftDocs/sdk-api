---
UID: NF:xpsobjectmodel.IXpsOMDashCollection.GetAt
title: IXpsOMDashCollection::GetAt
author: windows-sdk-content
description: Gets an XPS_DASH structure from a specified location in the collection.
old-location: xps\ixpsomdashcollection_getat.htm
old-project: printdocs
ms.assetid: 70749e4c-1f67-41e8-9def-85d38493c099
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMDashCollection interface, IXpsOMDashCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMDashCollection.GetAt, IXpsOMDashCollection::GetAt, xps.ixpsomdashcollection_getat, xpsobjectmodel/IXpsOMDashCollection::GetAt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMDashCollection.GetAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDashCollection::GetAt


## -description


Gets an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure is to  be obtained.


### -param dash [out, retval]

The <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure that is found at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/02a152a1-e117-42fb-8428-a2b28e6540a9">IXpsOMDashCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a>
 

 

