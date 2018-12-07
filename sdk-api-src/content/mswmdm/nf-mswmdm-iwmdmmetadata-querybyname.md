---
UID: NF:mswmdm.IWMDMMetaData.QueryByName
title: IWMDMMetaData::QueryByName
author: windows-sdk-content
description: The QueryByName method retrieves the value of a property specified by name.
old-location: wmdm\iwmdmmetadata_querybyname.htm
tech.root: WMDM
ms.assetid: e793954b-6aef-4088-97cb-eb1f050cc64b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMDMMetaData interface [windows Media Device Manager],QueryByName method, IWMDMMetaData.QueryByName, IWMDMMetaData::QueryByName, IWMDMMetaDataQueryByName, QueryByName, QueryByName method [windows Media Device Manager], QueryByName method [windows Media Device Manager],IWMDMMetaData interface, mswmdm/IWMDMMetaData::QueryByName, wmdm.iwmdmmetadata_querybyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMMetaData.QueryByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMMetaData::QueryByName


## -description



The <b>QueryByName</b> method retrieves the value of a property specified by name.




## -parameters




### -param pwszTagName [in]

Pointer to a wide-character <b>null</b>-terminated string specifying the property name. A list of standard property name constants is given in <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.


### -param pType [out]

An <a href="https://msdn.microsoft.com/9c300814-5610-4e46-b441-e7f2fc78a47b">WMDM_TAG_DATATYPE</a> enumerated value describing the type of data retrieved by <i>pValue</i>.


### -param pValue [out]

Pointer to a pointer to a byte array that receives the content of the value if the method succeeds. Windows Media Device Manager allocates this memory and the caller must free it using <b>CoTaskMemFree</b>.


### -param pcbLength [out]

Pointer to the size, in bytes, of the byte array <i>ppValue</i>. If the value is a string, this includes the termination character.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>



<a href="https://msdn.microsoft.com/5d27e1e9-ab91-433d-8216-ace195386d44">QueryByIndex</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 

