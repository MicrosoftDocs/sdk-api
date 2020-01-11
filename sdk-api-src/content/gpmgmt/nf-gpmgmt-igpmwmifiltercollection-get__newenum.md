---
UID: NF:gpmgmt.IGPMWMIFilterCollection.get__NewEnum
title: IGPMWMIFilterCollection::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection.
old-location: gpmc\igpmwmifiltercollection_get__newenum.htm
tech.root: gpmc
ms.assetid: acba6a75-9338-49b8-b04b-829f527d92ce
ms.date: 12/05/2018
ms.keywords: IGPMWMIFilterCollection interface [GPMC],get__NewEnum method, IGPMWMIFilterCollection.get__NewEnum, IGPMWMIFilterCollection::get__NewEnum, _win32_igpmwmifiltercollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMWMIFilterCollection interface, gpmc.igpmwmifiltercollection_get__newenum, gpmgmt/IGPMWMIFilterCollection::get__NewEnum
f1_keywords:
- gpmgmt/IGPMWMIFilterCollection.get__NewEnum
dev_langs:
- c++
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gpmgmt.dll
api_name:
- IGPMWMIFilterCollection.get__NewEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMWMIFilterCollection::get__NewEnum


## -description


Retrieves an enumerator for the collection.


## -parameters




### -param pVal [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>
 

 

