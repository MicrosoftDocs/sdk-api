---
UID: NF:cluadmex.IWEExtendPropertySheet.CreatePropertySheetPages
title: IWEExtendPropertySheet::CreatePropertySheetPages
author: windows-sdk-content
description: Creates property pages for a cluster object and adds them to a Failover Cluster Administrator property sheet.
old-location: mscs\iweextendpropertysheet_createpropertysheetpages.htm
old-project: mscs
ms.assetid: 00eca370-a2c6-4f5c-94a9-7d7e4334ccd5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreatePropertySheetPages, CreatePropertySheetPages method [Failover Cluster], CreatePropertySheetPages method [Failover Cluster],IWEExtendPropertySheet interface, IWEExtendPropertySheet interface [Failover Cluster],CreatePropertySheetPages method, IWEExtendPropertySheet.CreatePropertySheetPages, IWEExtendPropertySheet::CreatePropertySheetPages, _wolf_iweextendpropertysheet_createpropertysheetpages, cluadmex/IWEExtendPropertySheet::CreatePropertySheetPages, mscs.iweextendpropertysheet_createpropertysheetpages
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: Sources
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
req.lib: 
req.dll: 
req.irql: 
---

# IWEExtendPropertySheet::CreatePropertySheetPages


## -description


Creates property pages for a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a> and 
    adds them to a <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> 
    property sheet.


## -parameters




### -param piData [in]


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer for retrieving information relating to the new 
       property pages. By calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method with the 
       <i>piData</i> pointer, the following interfaces are available:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370234(v=VS.85).aspx">IGetClusterUIInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370211(v=VS.85).aspx">IGetClusterDataInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370224(v=VS.85).aspx">IGetClusterObjectInfo</a>
</li>
</ul>
Depending on the type of <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a> for 
       which property sheet pages are being created, a pointer to one of the following interfaces is also 
       available:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370221(v=VS.85).aspx">IGetClusterNodeInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370219(v=VS.85).aspx">IGetClusterNetworkInfo</a>, if the property 
        page relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370217(v=VS.85).aspx">IGetClusterNetInterfaceInfo</a>, if the 
        property page relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>, if the property 
        page relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>.</li>
</ul>

### -param piCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa370507(v=VS.85).aspx">IWCPropertySheetCallback</a> 
       interface implementation for adding property pages to the Cluster Administrator property sheet.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks




<a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> calls 
     an extension's 
     <b>CreatePropertySheetPages</b> 
     method to extend a property sheet to handle an additional 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster object</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>For each property page to be added</b>

<ol>
<li>Use <i>piData</i> to call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> and retrieve an 
       interface pointer for the cluster object associated with the page. For example, if you are adding a property 
       page for a resource, you want to retrieve a pointer to the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a> interface. 
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
       <a href="https://msdn.microsoft.com/en-us/library/Aa370509(v=VS.85).aspx">IWCPropertySheetCallback::AddPropertySheetPage</a> 
       method pointed to by <i>piCallback</i>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370211(v=VS.85).aspx">IGetClusterDataInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370217(v=VS.85).aspx">IGetClusterNetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370219(v=VS.85).aspx">IGetClusterNetworkInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370221(v=VS.85).aspx">IGetClusterNodeInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370224(v=VS.85).aspx">IGetClusterObjectInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370234(v=VS.85).aspx">IGetClusterUIInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370507(v=VS.85).aspx">IWCPropertySheetCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370509(v=VS.85).aspx">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="https://msdn.microsoft.com/1f2b7760-24d3-44a7-96a0-87e153b4bf92">IWEExtendPropertySheet</a>
 

 

