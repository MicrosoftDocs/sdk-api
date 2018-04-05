---
UID: NF:cluadmex.IWEExtendWizard97.CreateWizard97Pages
title: IWEExtendWizard97::CreateWizard97Pages method
author: windows-driver-content
description: Allows you to create Wizard97 property pages and add them to a Failover Cluster Administrator Wizard.
old-location: mscs\iweextendwizard97_createwizard97pages.htm
old-project: MsCS
ms.assetid: 1ab81008-42d8-4863-8836-0508e49ceca9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreateWizard97Pages method [Failover Cluster], CreateWizard97Pages method [Failover Cluster], IWEExtendWizard97 interface, CreateWizard97Pages,IWEExtendWizard97.CreateWizard97Pages, IWEExtendWizard97, IWEExtendWizard97 interface [Failover Cluster], CreateWizard97Pages method, IWEExtendWizard97::CreateWizard97Pages, _wolf_iweextendwizard97_createwizard97pages, cluadmex/IWEExtendWizard97::CreateWizard97Pages, mscs.iweextendwizard97_createwizard97pages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cluadmex.h
api_name:
-	IWEExtendWizard97.CreateWizard97Pages
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWEExtendWizard97::CreateWizard97Pages method


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create Wizard97 property pages and add them to a 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> Wizard.


## -parameters




### -param piData [in]


<a href="_com_iunknown">IUnknown</a> interface pointer for retrieving information 
       relating to the wizard97 pages to be added. By calling 
       <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> with the 
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
Depending on the type of <a href="c_gly.htm">cluster object</a>, a 
       pointer to one of the following interfaces is also available:

<ul>
<li>
<a href="https://msdn.microsoft.com/97c90830-1f6d-4f8f-ba0a-fee39aef5c1d">IGetClusterNodeInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.</li>
<li>
<a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>.</li>
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

Pointer to an <a href="https://msdn.microsoft.com/cbde3bcf-8242-49dc-9ac0-a4b078ea526e">IWCWizard97Callback</a> interface 
       implementation used to add the new Wizard97 property pages to the wizard.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If your extension has no Wizard97 pages but does have non-Wizard97 pages, you can either:

<ul>
<li>Support only the <a href="https://msdn.microsoft.com/6407163e-a8ca-4601-88a0-ecf87e29b9ab">IWEExtendWizard</a> interface.</li>
<li>Support both the <a href="https://msdn.microsoft.com/6407163e-a8ca-4601-88a0-ecf87e29b9ab">IWEExtendWizard</a> and 
       <a href="https://msdn.microsoft.com/3473dc89-8676-4b13-b3c8-f112c0b9cf8c">IWEExtendWizard97</a> interfaces, but in your 
       implementation of <b>IWEExtendWizard97</b>, query for the 
       <a href="https://msdn.microsoft.com/0d5f45c4-6091-4ea4-875a-69be7f1258db">IWCWizardCallback</a> interface from the interface 
       passed in by way of the <i>piCallback</i> parameter.</li>
</ul>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>For each Wizard97 property page to be added</b>

<ol>
<li>Use <i>piData</i> to call <a href="_com_IUnknown_QueryInterface">QueryInterface</a> and retrieve an 
       interface pointer for the <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">object</a> associated with the new 
       page. For example, if you are adding a property page for a resource, you want to retrieve a pointer to the 
       <a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the object being 
       extended, you should expect to receive errors when you attempt to call the methods.</li>
<li>To create the page, call the function 
       <a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new wizard97 page should be no larger than 293 
       dialog units wide and 172 dialog units high, and should contain a static control positioned at (38,12) with a 
       size of (247,10).</li>
<li>To add the page to a Cluster Administrator Wizard, call 
       <a href="https://msdn.microsoft.com/c5de70da-2a08-4142-8f21-53a98e28fd42">IWCWizard97Callback::AddWizard97Page</a> 
       using the <i>piCallback</i> pointer.</li>
</ol>



## -see-also




<a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a>



<a href="https://msdn.microsoft.com/a2800ac8-a865-4e66-8147-90e95b54cb0c">IGetClusterDataInfo</a>



<a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>



<a href="https://msdn.microsoft.com/c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79">IGetClusterNetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/7c304d9c-69b6-48fc-bb1b-f49d1ac8ede4">IGetClusterNetworkInfo</a>



<a href="https://msdn.microsoft.com/97c90830-1f6d-4f8f-ba0a-fee39aef5c1d">IGetClusterNodeInfo</a>



<a href="https://msdn.microsoft.com/a88ba05c-b64b-4d6d-b005-f2f867093355">IGetClusterObjectInfo</a>



<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>



<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>



<a href="https://msdn.microsoft.com/ccd87d3a-c9da-4d61-9e9b-f25a52724166">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="https://msdn.microsoft.com/0d5f45c4-6091-4ea4-875a-69be7f1258db">IWCWizardCallback</a>



<a href="https://msdn.microsoft.com/6407163e-a8ca-4601-88a0-ecf87e29b9ab">IWEExtendWizard</a>



<a href="https://msdn.microsoft.com/3473dc89-8676-4b13-b3c8-f112c0b9cf8c">IWEExtendWizard97</a>
 

 

