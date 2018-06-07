---
UID: NF:sdoias.ISdoCollection.Add
title: ISdoCollection::Add
author: windows-sdk-content
description: The Add method adds an item to the Server Data Objects (SDO) collection.
old-location: nps\SDO_isdocollection_add.htm
old-project: Nps
ms.assetid: a575b224-9827-47f3-a819-bd793200c901
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: Add, Add method [Network Policy Server], Add method [Network Policy Server],ISdoCollection interface, ISdoCollection interface [Network Policy Server],Add method, ISdoCollection.Add, ISdoCollection::Add, _sdo_isdocollection_add, nps.SDO_isdocollection_add, sdo.isdocollection_add, sdoias/ISdoCollection::Add
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VENDORPROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoCollection.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISdoCollection::Add


## -description


The 
<b>Add</b> method adds an item to the Server Data Objects (SDO) collection.


## -parameters




### -param bstrName [in]

Specifies the name of the SDO Object. This parameter may be <b>NULL</b>.


### -param ppItem [in, out]

Pointer to an <b>IDispatch</b> interface pointer for the Item to add. This parameter must not be <b>NULL</b>.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



If you specify the name of the object to add, ensure that the name is unique by calling 
<a href="https://msdn.microsoft.com/cf9263c3-5d98-4b52-bbd7-6a37fb4c8481">ISdoCollection::IsNameUnique</a>.

If the <i>bstrName</i> parameter is not specified, <b>ISdoCollection::Add</b> obtains it from the object specified by the <i>ppItem</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/fc62698d-0bb9-478c-91cf-9f8fec36dba4">Adding an Object to a Collection</a>



<a href="https://msdn.microsoft.com/library/windows/desktop/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>



<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>



<a href="https://msdn.microsoft.com/26470906-1cba-41fc-96f3-078208ab3d51">ISdoCollection</a>



<a href="https://msdn.microsoft.com/cf9263c3-5d98-4b52-bbd7-6a37fb4c8481">ISdoCollection::IsNameUnique</a>
 

 

