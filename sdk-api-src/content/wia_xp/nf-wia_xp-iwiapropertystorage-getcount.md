---
UID: NF:wia_xp.IWiaPropertyStorage.GetCount
title: IWiaPropertyStorage::GetCount
author: windows-sdk-content
description: The IWiaPropertyStorage::GetCount method returns the number of properties stored in the property storage.
old-location: wia\_wia_IWiaPropertyStorage_GetCount.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\getcount.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCount, GetCount method [WIA], GetCount method [WIA],IWiaPropertyStorage interface, IWiaPropertyStorage interface [WIA],GetCount method, IWiaPropertyStorage.GetCount, IWiaPropertyStorage::GetCount, _wia_IWiaPropertyStorage_GetCount, wia._wia_IWiaPropertyStorage_GetCount, wia_xp/IWiaPropertyStorage::GetCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
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
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaPropertyStorage.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wia_xp.h
: 
- IWiaPropertyStorage.GetCount
: 
---

# IWiaPropertyStorage::GetCount


## -description


The <b>IWiaPropertyStorage::GetCount</b> method returns the number of properties stored in the property storage.


## -parameters




### -param pulNumProps [out]

Type: <b>ULONG*</b>

Receives the number of properties stored in the property storage.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms629938(v=VS.85).aspx">IWiaPropertyStorage</a>
 

 

