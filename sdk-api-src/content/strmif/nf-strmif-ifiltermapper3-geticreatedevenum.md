---
UID: NF:strmif.IFilterMapper3.GetICreateDevEnum
title: IFilterMapper3::GetICreateDevEnum
author: windows-sdk-content
description: The GetICreateDevEnum method returns a pointer to the ICreateDevEnum interface. You can use the ICreateDevEnum interface to create an enumerator for a category of filters, such as video capture devices or audio capture devices.
old-location: dshow\ifiltermapper3_geticreatedevenum.htm
tech.root: DirectShow
ms.assetid: e54a1276-5c86-4127-9005-f2935e1664d0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetICreateDevEnum, GetICreateDevEnum method [DirectShow], GetICreateDevEnum method [DirectShow],IFilterMapper3 interface, IFilterMapper3 interface [DirectShow],GetICreateDevEnum method, IFilterMapper3.GetICreateDevEnum, IFilterMapper3::GetICreateDevEnum, IFilterMapper3GetICreateDevEnum, dshow.ifiltermapper3_geticreatedevenum, strmif/IFilterMapper3::GetICreateDevEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper3.GetICreateDevEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterMapper3::GetICreateDevEnum


## -description



The <code>GetICreateDevEnum</code> method returns a pointer to the <b>ICreateDevEnum</b> interface. You can use the <a href="https://msdn.microsoft.com/fc300bb8-aea4-4848-af43-a70a7fb8c07c">ICreateDevEnum</a> interface to create an enumerator for a category of filters, such as video capture devices or audio capture devices.


<div class="alert"><b>Note</b>  This method is deprecated. Instead, applications should call <b>CoCreateInstance</b> with CLSID_SystemDeviceEnum to create the <a href="https://msdn.microsoft.com/ea98be7f-580d-4986-bd6b-d254a2c075e8">System Device Enumerator</a>.</div><div> </div>

## -parameters




### -param ppEnum [out]

Receives a pointer to the <b>ICreateDevEnum</b> interface. The caller must release the interface.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/385a4d15-08b5-40c6-8444-a22bec86a981">IFilterMapper3 Interface</a>
 

 

