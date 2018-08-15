---
UID: NF:wia_xp.IWiaPropertyStorage.GetPropertyStream
title: IWiaPropertyStorage::GetPropertyStream
author: windows-sdk-content
description: The IWiaPropertyStorage::GetPropertyStream method retrieves the property stream of an item.
old-location: wia\_wia_IWiaPropertyStorage_GetPropertyStream.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\getpropertystream.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetPropertyStream, GetPropertyStream method [WIA], GetPropertyStream method [WIA],IWiaPropertyStorage interface, IWiaPropertyStorage interface [WIA],GetPropertyStream method, IWiaPropertyStorage.GetPropertyStream, IWiaPropertyStorage::GetPropertyStream, _wia_IWiaPropertyStorage_GetPropertyStream, wia._wia_IWiaPropertyStorage_GetPropertyStream, wia_xp/IWiaPropertyStorage::GetPropertyStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaPropertyStorage.GetPropertyStream
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaPropertyStorage::GetPropertyStream


## -description


The <b>IWiaPropertyStorage::GetPropertyStream</b> method retrieves the property stream of an item.


## -parameters




### -param pCompatibilityId




### -param ppIStream [out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

Pointer to a stream that receives the item properties. For more information, see <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.


#### - pCompatibilityID [out]

Type: <b>GUID*</b>

Receives a unique identifier for a set of property values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications use this method to get a snapshot of the current properties of an item. These are subsequently restored by calling <a href="https://msdn.microsoft.com/44f25d8c-7f83-4c36-b582-abb6678ed78e">IWiaPropertyStorage::SetPropertyStream</a>.

Applications can use the <i>pCompatibilityID</i> parameter to check if a device supports a specific set of property values before attempting to write these values to the device.

When it is finished using the item's property stream, the application must release it.




## -see-also




<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/b80d22d4-8e36-484a-9dd1-f228e2236eaf">IWiaPropertyStorage</a>
 

 

