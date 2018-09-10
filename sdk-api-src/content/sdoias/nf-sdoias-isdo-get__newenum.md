---
UID: NF:sdoias.ISdo.get__NewEnum
title: ISdo::get__NewEnum
author: windows-sdk-content
description: The get__NewEnum method retrieves an IEnumVARIANT interface for the Server Data Objects (SDO) properties.
old-location: nps\SDO_isdo_get__newenum.htm
tech.root: nps
ms.assetid: 23033dc3-824c-429c-836d-65782ca3df92
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISdo interface [Network Policy Server],get__NewEnum method, ISdo.get__NewEnum, ISdo::get__NewEnum, _sdo_isdo_get__newenum, get__NewEnum, get__NewEnum method [Network Policy Server], get__NewEnum method [Network Policy Server],ISdo interface, nps.SDO_isdo_get__newenum, sdo.isdo_get__newenum, sdoias/ISdo::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISdo.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdo::get__NewEnum


## -description


The 
<b>get__NewEnum</b> method retrieves an 
<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface for the Server Data Objects (SDO) properties.


## -parameters




### -param ppEnumVARIANT [out]

Pointer to a pointer that, on successful return, points to an 
<a href="_com_iunknown">IUnknown</a> interface pointer. Use this <b>IUnknown</b> interface pointer with 
its <a href="_com_iunknown_queryinterface">QueryInterface</a> method to obtain an 
<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



<div class="alert"><b>Note</b>  Two underscores are used between "get" and "NewEnum" in the name of this method.</div>
<div> </div>



## -see-also




<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>



<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>
 

 

