---
UID: NF:mswmdm.IWMDMMetaData.AddItem
title: IWMDMMetaData::AddItem
author: windows-sdk-content
description: The AddItem method adds a metadata property to the interface.
old-location: wmdm\iwmdmmetadata_additem.htm
old-project: WMDM
ms.assetid: fb8dee5f-034f-4e1d-86fe-34a2d9439e5f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AddItem, AddItem method [windows Media Device Manager], AddItem method [windows Media Device Manager],IWMDMMetaData interface, IWMDMMetaData interface [windows Media Device Manager],AddItem method, IWMDMMetaData.AddItem, IWMDMMetaData::AddItem, IWMDMMetaDataAddItem, mswmdm/IWMDMMetaData::AddItem, wmdm.iwmdmmetadata_additem
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMMetaData.AddItem
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMMetaData::AddItem


## -description



The <b>AddItem</b> method adds a metadata property to the interface.




## -parameters




### -param Type [in]

An <a href="https://msdn.microsoft.com/9c300814-5610-4e46-b441-e7f2fc78a47b">WMDM_TAG_DATATYPE</a> enumerated value specifying the type of metadata being saved.


### -param pwszTagName [in]

Pointer to a wide-character, null-terminated string specifying the name of the property to set. A list of standard property name constants is given in <a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>.


### -param pValue [in]

Pointer to a byte array specifying the value to assign to the property. The submitted value is copied, so the memory can be freed after calling <b>AddItem</b>.


### -param iLength [in]

Integer specifying the size of <i>pValue</i>, in bytes.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 

