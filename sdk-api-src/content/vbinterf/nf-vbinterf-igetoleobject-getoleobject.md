---
UID: NF:vbinterf.IGetOleObject.GetOleObject
title: IGetOleObject::GetOleObject
author: windows-sdk-content
description: Gets a pointer to an OLE control on a Visual Basic container.
old-location: com\igetoleobject_getoleobject.htm
tech.root: com
ms.assetid: eafb9dbc-ab46-4b83-8be9-6c8cd1de8ab3
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetOleObject, GetOleObject method [COM], GetOleObject method [COM],IGetOleObject interface, IGetOleObject interface [COM],GetOleObject method, IGetOleObject.GetOleObject, IGetOleObject::GetOleObject, _com_IGetOleObject_GetOleObject, com.igetoleobject_getoleobject, vbinterf/IGetOleObject::GetOleObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vbinterf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - COM
api_location:
 - VbInterf.h
api_name:
 - IGetOleObject.GetOleObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetOleObject::GetOleObject


## -description


Gets a pointer to an OLE control on a Visual Basic container.
<div class="alert"><b>Note</b>  The use of this method is no longer recommended because containers other than Visual Basic do not support 
    it.</div><div> </div>

## -parameters




### -param riid [in]

Specifies the interface to retrieve. Pass <b>IID_IOleObject</b> to obtain a pointer to 
      the control.


### -param ppvObj [out]

Pointer to the control.


## -returns



This method supports the standard return values <b>E_INVALIDARG</b>, 
      <b>E_OUTOFMEMORY</b>, and <b>E_UNEXPECTED</b>, as well as the 
      following:




## -see-also




<a href="https://msdn.microsoft.com/2cdc35e7-ab0b-4b12-920c-9eac0d9b5a0c">IGetOleObject</a>
 

 

