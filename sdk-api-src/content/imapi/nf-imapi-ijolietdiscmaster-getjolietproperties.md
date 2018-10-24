---
UID: NF:imapi.IJolietDiscMaster.GetJolietProperties
title: IJolietDiscMaster::GetJolietProperties
author: windows-sdk-content
description: Retrieves a pointer to an IPropertyStorage interface that contains the Joliet properties.
old-location: imapi\ijolietdiscmaster_getjolietproperties.htm
tech.root: imapi
ms.assetid: 660657b3-b378-4c16-9294-89309e4da569
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetJolietProperties, GetJolietProperties method [IMAPI], GetJolietProperties method [IMAPI],IJolietDiscMaster interface, IJolietDiscMaster interface [IMAPI],GetJolietProperties method, IJolietDiscMaster.GetJolietProperties, IJolietDiscMaster::GetJolietProperties, _win32_ijolietdiscmaster_getjolietproperties, base.ijolietdiscmaster_getjolietproperties, imapi.ijolietdiscmaster_getjolietproperties, imapi/IJolietDiscMaster::GetJolietProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IJolietDiscMaster.GetJolietProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IJolietDiscMaster::GetJolietProperties


## -description


Retrieves a pointer to an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface that contains the Joliet properties.


## -parameters




### -param ppPropStg [out]

Address of a pointer to an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface for the Joliet property set with all current properties defined.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Properties are not retained after IMAPI is closed. A property set is convenient for IMAPI because it stores an ID/TYPE/VALUE combination, as well as ID/NAME associations. Each combination is a single property, and IMAPI uses these properties as values that are unique to the Joliet interface. For example, the Joliet interface supports a VolumeName property.

The caller can modify these properties by calling 
<a href="https://msdn.microsoft.com/467f8fb8-2a82-46d2-b304-3c3a600a9c63">SetJolietProperties</a>. Current properties include the following.






## -see-also




<a href="https://msdn.microsoft.com/e2269b68-1860-4afd-90f2-d61297f3fa9b">IJolietDiscMaster</a>



<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

