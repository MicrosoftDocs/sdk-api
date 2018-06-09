---
UID: NF:mfobjects.IMFAttributes.SetItem
title: IMFAttributes::SetItem
author: windows-sdk-content
description: Adds an attribute value with a specified key.
old-location: mf\imfattributes_setitem.htm
old-project: medfound
ms.assetid: 1ac6e1c3-cf78-4cff-a992-4f92f243c443
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 1ac6e1c3-cf78-4cff-a992-4f92f243c443, IMFAttributes interface [Media Foundation],SetItem method, IMFAttributes.SetItem, IMFAttributes::SetItem, SetItem, SetItem method [Media Foundation], SetItem method [Media Foundation],IMFAttributes interface, mf.imfattributes_setitem, mfobjects/IMFAttributes::SetItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.SetItem
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::SetItem


## -description



          Adds an attribute value with a specified key.
        


## -parameters




### -param guidKey [in]


            A GUID that identifies the value to set. If this key already exists, the method overwrites the old value.
          


### -param Value [in]


            
              A <b>PROPVARIANT</b> that contains the attribute value. The method copies the value. The <b>PROPVARIANT</b> type must be one of the types listed in the <a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a> enumeration.
          


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">

                Insufficient memory.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">

                Invalid attribute type.
              

</td>
</tr>
</table>
 




## -remarks




        This method checks whether the <b>PROPVARIANT</b> type is one of the attribute types defined in <a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a>, and fails if an unsupported type is used. However, this method does not check whether the <b>PROPVARIANT</b> is the correct type for the specified attribute GUID. (There is no programmatic way to associate attribute GUIDs with property types.) For a list of Media Foundation attributes and their data types, see <a href="https://msdn.microsoft.com/445fc879-3c9e-409d-8d05-ecd1ff9afc19">Media Foundation Attributes</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 

