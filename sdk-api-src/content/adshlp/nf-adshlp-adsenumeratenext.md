---
UID: NF:adshlp.ADsEnumerateNext
title: ADsEnumerateNext function (adshlp.h)
author: windows-sdk-content
description: The ADsEnumerateNext function enumerates through a specified number of elements from the current cursor position of the enumerator.
old-location: adsi\adsenumeratenext.htm
tech.root: adsi
ms.assetid: 9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADsEnumerateNext, ADsEnumerateNext function [ADSI], _ds_adsenumeratenext, adshlp/ADsEnumerateNext, adsi.adsenumeratenext
ms.topic: function
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsEnumerateNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ADsEnumerateNext function


## -description


The <b>ADsEnumerateNext</b> function enumerates through a specified number of elements from the current cursor position of the enumerator. When the operation succeeds, the function returns the enumerated set of elements in a variant array. The number of returned elements can be smaller than the specified number.


## -parameters




### -param pEnumVariant [in]

Type: <b>IEnumVARIANT*</b>

Pointer to the  <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface on the enumerator object.


### -param cElements [in]

Type: <b>ULONG</b>

Number of elements requested.


### -param pvar [out]

Type: <b>VARIANT*</b>

Pointer to the array of elements retrieved.


### -param pcElementsFetched [out]

Type: <b>ULONG*</b>

Actual number of elements retrieved, which can be smaller than the number of elements requested.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values.

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The general process to enumerate objects in a container involves the following:

First, create an enumerator object on that container.

Second, retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface pointer.

Third, call the <b>ADsEnumerateNext</b> function to return an enumerated set of elements from the enumerator object.

Fourth, call the <a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADSFreeEnumerator</a> function to free the enumerator object.

For more information and a code example, see the  <a href="https://msdn.microsoft.com/e4fdec19-bccf-49ec-8a95-29e096c4c9c1">ADsBuildEnumerator</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/e4fdec19-bccf-49ec-8a95-29e096c4c9c1">ADsBuildEnumerator</a>



<a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADsFreeEnumerator</a>



<a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a>
 

 

