---
UID: NF:cluadmex.IWEExtendPropertySheet.CreatePropertySheetPages
title: IWEExtendPropertySheet::CreatePropertySheetPages
author: windows-sdk-content
description: Creates property pages for a cluster object and adds them to a Failover Cluster Administrator property sheet.
old-location: mscs\iweextendpropertysheet_createpropertysheetpages.htm
tech.root: mscs
ms.assetid: 00eca370-a2c6-4f5c-94a9-7d7e4334ccd5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreatePropertySheetPages, CreatePropertySheetPages method [Failover Cluster], CreatePropertySheetPages method [Failover Cluster],IWEExtendPropertySheet interface, IWEExtendPropertySheet interface [Failover Cluster],CreatePropertySheetPages method, IWEExtendPropertySheet.CreatePropertySheetPages, IWEExtendPropertySheet::CreatePropertySheetPages, _wolf_iweextendpropertysheet_createpropertysheetpages, cluadmex/IWEExtendPropertySheet::CreatePropertySheetPages, mscs.iweextendpropertysheet_createpropertysheetpages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
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
 - cluadmex.h
api_name:
 - IWEExtendPropertySheet.CreatePropertySheetPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWEExtendPropertySheet::CreatePropertySheetPages


## -description


Creates property pages for a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a> and 
    adds them to a <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> 
    property sheet.


## -parameters




### -param piData [in]


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer for retrieving information relating to the new 
       property pages. By calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method with the 
       <i>piData</i> pointer, the following interfaces are available:

<ul>
<li>
<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a2800ac8-a865-4e66-8147-90e95b54cb0c">IGetClusterDataInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a88ba05c-b64b-4d6d-b005-f2f867093355">IGetClusterObjectInfo</a>
</li>
</ul>
Depending on the type of <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a> for 
       which property sheet pages are being created, a pointer to one of the following interfaces is also 
       available:

<ul>
<li>
<a href="https://msdn.microsoft.com/97c90830-1f6d-4f8f-ba0a-fee39aef5c1d">IGetClusterNodeInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.</li>
<li>
<a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a>.</li>
<li>
<a href="https://msdn.microsoft.com/7c304d9c-69b6-48fc-bb1b-f49d1ac8ede4">IGetClusterNetworkInfo</a>, if the property 
        page relates to a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>.</li>
<li>
<a href="https://msdn.microsoft.com/c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79">IGetClusterNetInterfaceInfo</a>, if the 
        property page relates to a <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>.</li>
<li>
<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>, if the property 
        page relates to a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.</li>
</ul>

### -param piCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/f90f9eb3-5568-4db1-8ff8-fda2d3bea952">IWCPropertySheetCallback</a> 
       interface implementation for adding property pages to the Cluster Administrator property sheet.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
At least one of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
<dt>0x80004001</dt>
</dl>
</td>
<td width="60%">
The extension does not support adding property pages.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> calls 
     an extension's 
     <b>CreatePropertySheetPages</b> 
     method to extend a property sheet to handle an additional 
     <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>For each property page to be added</b>

<ol>
<li>Use <i>piData</i> to call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> and retrieve an 
       interface pointer for the cluster object associated with the page. For example, if you are adding a property 
       page for a resource, you want to retrieve a pointer to the 
       <a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the target object, 
       you should expect to receive errors when you attempt to call the methods.</li>
<li>
To create the page, call the function 
       <a href="https://msdn.microsoft.com/en-us/library/Bb760807(v=VS.85).aspx">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new property page should be no larger than 252 
       dialog units wide and 218 dialog units high, and should contain two standard controls:

<ul>
<li>For the object icon, an icon control positioned at (8,7) with a size of (18,20).</li>
<li>For the object name, a static control positioned at (38,12) with a size of (206,10).</li>
</ul>
</li>
<li>To add the page to the property sheet, call the 
       <a href="https://msdn.microsoft.com/ccd87d3a-c9da-4d61-9e9b-f25a52724166">IWCPropertySheetCallback::AddPropertySheetPage</a> 
       method pointed to by <i>piCallback</i>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/a2800ac8-a865-4e66-8147-90e95b54cb0c">IGetClusterDataInfo</a>



<a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>



<a href="https://msdn.microsoft.com/c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79">IGetClusterNetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/7c304d9c-69b6-48fc-bb1b-f49d1ac8ede4">IGetClusterNetworkInfo</a>



<a href="https://msdn.microsoft.com/97c90830-1f6d-4f8f-ba0a-fee39aef5c1d">IGetClusterNodeInfo</a>



<a href="https://msdn.microsoft.com/a88ba05c-b64b-4d6d-b005-f2f867093355">IGetClusterObjectInfo</a>



<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>



<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>



<a href="https://msdn.microsoft.com/f90f9eb3-5568-4db1-8ff8-fda2d3bea952">IWCPropertySheetCallback</a>



<a href="https://msdn.microsoft.com/ccd87d3a-c9da-4d61-9e9b-f25a52724166">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="https://msdn.microsoft.com/1f2b7760-24d3-44a7-96a0-87e153b4bf92">IWEExtendPropertySheet</a>
 

 

