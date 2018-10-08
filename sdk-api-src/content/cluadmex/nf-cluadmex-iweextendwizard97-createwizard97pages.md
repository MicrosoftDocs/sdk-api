---
UID: NF:cluadmex.IWEExtendWizard97.CreateWizard97Pages
title: IWEExtendWizard97::CreateWizard97Pages
author: windows-sdk-content
description: Allows you to create Wizard97 property pages and add them to a Failover Cluster Administrator Wizard.
old-location: mscs\iweextendwizard97_createwizard97pages.htm
tech.root: MsCS
ms.assetid: 1ab81008-42d8-4863-8836-0508e49ceca9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateWizard97Pages, CreateWizard97Pages method [Failover Cluster], CreateWizard97Pages method [Failover Cluster],IWEExtendWizard97 interface, IWEExtendWizard97 interface [Failover Cluster],CreateWizard97Pages method, IWEExtendWizard97.CreateWizard97Pages, IWEExtendWizard97::CreateWizard97Pages, _wolf_iweextendwizard97_createwizard97pages, cluadmex/IWEExtendWizard97::CreateWizard97Pages, mscs.iweextendwizard97_createwizard97pages
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
 - IWEExtendWizard97.CreateWizard97Pages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWEExtendWizard97::CreateWizard97Pages


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create Wizard97 property pages and add them to a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> Wizard.


## -parameters




### -param piData [in]


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer for retrieving information 
       relating to the wizard97 pages to be added. By calling 
       <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> with the 
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
Depending on the type of <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a>, a 
       pointer to one of the following interfaces is also available:

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

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa370511(v=VS.85).aspx">IWCWizard97Callback</a> interface 
       implementation used to add the new Wizard97 property pages to the wizard.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If your extension has no Wizard97 pages but does have non-Wizard97 pages, you can either:

<ul>
<li>Support only the <a href="https://msdn.microsoft.com/en-us/library/Aa370724(v=VS.85).aspx">IWEExtendWizard</a> interface.</li>
<li>Support both the <a href="https://msdn.microsoft.com/en-us/library/Aa370724(v=VS.85).aspx">IWEExtendWizard</a> and 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370728(v=VS.85).aspx">IWEExtendWizard97</a> interfaces, but in your 
       implementation of <b>IWEExtendWizard97</b>, query for the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370517(v=VS.85).aspx">IWCWizardCallback</a> interface from the interface 
       passed in by way of the <i>piCallback</i> parameter.</li>
</ul>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>For each Wizard97 property page to be added</b>

<ol>
<li>Use <i>piData</i> to call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> and retrieve an 
       interface pointer for the <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">object</a> associated with the new 
       page. For example, if you are adding a property page for a resource, you want to retrieve a pointer to the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the object being 
       extended, you should expect to receive errors when you attempt to call the methods.</li>
<li>To create the page, call the function 
       <a href="https://msdn.microsoft.com/en-us/library/Bb760807(v=VS.85).aspx">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new wizard97 page should be no larger than 293 
       dialog units wide and 172 dialog units high, and should contain a static control positioned at (38,12) with a 
       size of (247,10).</li>
<li>To add the page to a Cluster Administrator Wizard, call 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370512(v=VS.85).aspx">IWCWizard97Callback::AddWizard97Page</a> 
       using the <i>piCallback</i> pointer.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb760807(v=VS.85).aspx">CreatePropertySheetPage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370211(v=VS.85).aspx">IGetClusterDataInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370217(v=VS.85).aspx">IGetClusterNetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370219(v=VS.85).aspx">IGetClusterNetworkInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370221(v=VS.85).aspx">IGetClusterNodeInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370224(v=VS.85).aspx">IGetClusterObjectInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370234(v=VS.85).aspx">IGetClusterUIInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370509(v=VS.85).aspx">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370517(v=VS.85).aspx">IWCWizardCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370724(v=VS.85).aspx">IWEExtendWizard</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370728(v=VS.85).aspx">IWEExtendWizard97</a>
 

 

