---
UID: NF:cluadmex.IWEExtendWizard.CreateWizardPages
title: IWEExtendWizard::CreateWizardPages
author: windows-driver-content
description: Allows you to create wizard pages and add them to Failover Cluster Administrator's New Resource Wizard or Cluster Application Wizard.
old-location: mscs\iweextendwizard_createwizardpages.htm
old-project: MsCS
ms.assetid: b52ea5a5-aa80-4f65-9bab-b60fa8363b01
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CreateWizardPages, CreateWizardPages method [Failover Cluster], CreateWizardPages method [Failover Cluster],IWEExtendWizard interface, IWEExtendWizard interface [Failover Cluster],CreateWizardPages method, IWEExtendWizard.CreateWizardPages, IWEExtendWizard::CreateWizardPages, _wolf_iweextendwizard_createwizardpages, cluadmex/IWEExtendWizard::CreateWizardPages, mscs.iweextendwizard_createwizardpages
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cluadmex.h
api_name:
-	IWEExtendWizard.CreateWizardPages
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWEExtendWizard::CreateWizardPages


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create wizard pages and add them to 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator's</a> New Resource Wizard 
     or Cluster Application Wizard.


## -parameters




### -param piData [in]


<a href="_com_iunknown">IUnknown</a> interface pointer for retrieving information 
       relating to the wizard pages to be added. By calling 
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
Depending on the type of <a href="c_gly.htm">cluster object</a> for 
       which the wizard page is being created, a pointer to one of the following interfaces is also available:

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

Pointer to an <a href="https://msdn.microsoft.com/0d5f45c4-6091-4ea4-875a-69be7f1258db">IWCWizardCallback</a> interface 
       implementation used to add the new property pages to the wizard.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks



To add Wizard97 wizard pages, use the 
     <a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a> 
     method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>For each property page to be added</b>

<ol>
<li>Use <i>piData</i> to call 
       <a href="_com_IUnknown_QueryInterface">QueryInterface</a> and retrieve an interface 
       pointer for the <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a> associated with the new 
       page. For example, if you are adding a property page for a resource, you want to retrieve a pointer to the 
       <a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the object being 
       extended, you should expect to receive errors when you attempt to call the methods.</li>
<li>
To create the page, call the function 
       <a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new property page should be no larger than 252 
       dialog units wide and 218 dialog units high, and should contain two standard controls:

<ul>
<li>For the object icon, an icon control positioned at (8,7) with a size of (18,20).</li>
<li>For the object name, a static control positioned at (38,12) with a size of (247,10).</li>
</ul>
</li>
<li>To add the page to a Cluster Administrator Wizard, call 
       <a href="https://msdn.microsoft.com/e5ce7798-c1e6-47b6-a1bf-1262b3511b22">IWCWizardCallback::AddWizardPage</a> 
       using the <i>piCallback</i> pointer.</li>
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



<a href="https://msdn.microsoft.com/ccd87d3a-c9da-4d61-9e9b-f25a52724166">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="https://msdn.microsoft.com/0d5f45c4-6091-4ea4-875a-69be7f1258db">IWCWizardCallback</a>



<a href="https://msdn.microsoft.com/6407163e-a8ca-4601-88a0-ecf87e29b9ab">IWEExtendWizard</a>



<a href="https://msdn.microsoft.com/3473dc89-8676-4b13-b3c8-f112c0b9cf8c">IWEExtendWizard97</a>



<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>
 

 

