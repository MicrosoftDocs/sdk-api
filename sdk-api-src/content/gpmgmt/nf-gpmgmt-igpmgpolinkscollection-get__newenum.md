---
UID: NF:gpmgmt.IGPMGPOLinksCollection.get__NewEnum
title: IGPMGPOLinksCollection::get__NewEnum
author: windows-sdk-content
description: The get_NewEnum method retrieves an enumerator for the collection.
old-location: gpmc\igpmgpolinkscollection_get__newenum.htm
tech.root: gpmc
ms.assetid: 953735c2-01d7-45e1-8417-6b18128de530
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IGPMGPOLinksCollection interface [GPMC],get__NewEnum method, IGPMGPOLinksCollection.get__NewEnum, IGPMGPOLinksCollection::get__NewEnum, _win32_igpmgpolinkscollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMGPOLinksCollection interface, gpmc.igpmgpolinkscollection_get__newenum, gpmgmt/IGPMGPOLinksCollection::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IGPMGPOLinksCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPOLinksCollection::get__NewEnum


## -description


The <b>get_NewEnum</b> method retrieves an enumerator for the collection.


## -parameters




### -param ppIGPMLinks [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/290a53fb-8be0-477d-837c-46251b30e245">IGPMGPOLink</a>



<a href="https://msdn.microsoft.com/37753a31-0ef8-4fb9-b542-a91ae47ed417">IGPMGPOLinksCollection</a>
 

 

