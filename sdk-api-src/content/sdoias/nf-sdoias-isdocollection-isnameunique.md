---
UID: NF:sdoias.ISdoCollection.IsNameUnique
title: ISdoCollection::IsNameUnique (sdoias.h)
author: windows-sdk-content
description: The IsNameUnique method tests whether the specified name is unique in the collection.
old-location: nps\SDO_isdocollection_isnameunique.htm
tech.root: Nps
ms.assetid: cf9263c3-5d98-4b52-bbd7-6a37fb4c8481
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISdoCollection interface [Network Policy Server],IsNameUnique method, ISdoCollection.IsNameUnique, ISdoCollection::IsNameUnique, IsNameUnique, IsNameUnique method [Network Policy Server], IsNameUnique method [Network Policy Server],ISdoCollection interface, _sdo_isdocollection_isnameunique, nps.SDO_isdocollection_isnameunique, sdo.isdocollection_isnameunique, sdoias/ISdoCollection::IsNameUnique
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
req.lib: 
req.dll: Iassdo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoCollection.IsNameUnique
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdoCollection::IsNameUnique


## -description


The 
<b>IsNameUnique</b> method tests whether the specified name is unique in the collection.


## -parameters




### -param bstrName [in]

Specifies the name to test.


### -param pBool [out]

Pointer to a <b>VARIANT</b> that specifies whether the name is unique. The returned value is <b>VARIANT_TRUE</b> if the name is unique, <b>VARIANT_FALSE</b> otherwise.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Neither of the parameters may be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/fc62698d-0bb9-478c-91cf-9f8fec36dba4">Adding an Object to a Collection</a>



<a href="https://msdn.microsoft.com/9c7ee4d7-987f-45ae-810f-fc310955f36d">IASCOMMONPROPERTIES</a>



<a href="https://msdn.microsoft.com/26470906-1cba-41fc-96f3-078208ab3d51">ISdoCollection</a>



<a href="https://msdn.microsoft.com/a575b224-9827-47f3-a819-bd793200c901">ISdoCollection::Add</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a>
 

 

