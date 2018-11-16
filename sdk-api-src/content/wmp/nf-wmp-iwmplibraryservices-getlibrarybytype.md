---
UID: NF:wmp.IWMPLibraryServices.getLibraryByType
title: IWMPLibraryServices::getLibraryByType
author: windows-sdk-content
description: The getLibraryByType method retrieves a pointer to an IWMPLibrary interface that represents the library that has the specified type and index.
old-location: wmp\iwmplibraryservices_getlibrarybytype.htm
tech.root: WMP
ms.assetid: 766cfd4e-53e6-44a8-87e6-2b9c1fa2ff3f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPLibraryServices interface [Windows Media Player],getLibraryByType method, IWMPLibraryServices.getLibraryByType, IWMPLibraryServices::getLibraryByType, IWMPLibraryServicesgetLibraryByType, getLibraryByType, getLibraryByType method [Windows Media Player], getLibraryByType method [Windows Media Player],IWMPLibraryServices interface, wmp.iwmplibraryservices_getlibrarybytype, wmp/IWMPLibraryServices::getLibraryByType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPLibraryServices.getLibraryByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPLibraryServices.getLibraryByType
: 
---

# IWMPLibraryServices::getLibraryByType


## -description



The <b>getLibraryByType</b> method retrieves a pointer to an <b>IWMPLibrary</b> interface that represents the library that has the specified type and index.




## -parameters




### -param wmplt [in]

<b>WMPLibraryType</b> enumeration value that specifies the type of library to retrieve.


### -param lIndex [in]

A <b>long</b> containing the index of the library to retrieve.


### -param ppIWMPLibrary [out]

Address of a variable that receives a pointer to the retrieved <b>IWMPLibrary</b> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



There is only one local library and disc libraries are available only on data CDs and DVDs that contain media content.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/add0ed43-d83f-4793-b1f6-ccad0f01854c">IWMPLibrary Interface</a>



<a href="https://msdn.microsoft.com/9ed6d02e-15ca-425f-8642-e32a5adfaa55">IWMPLibraryServices Interface</a>



<a href="https://msdn.microsoft.com/bf0e7140-5a33-4841-bd55-ac07dae09c41">WMPLibraryType</a>
 

 

