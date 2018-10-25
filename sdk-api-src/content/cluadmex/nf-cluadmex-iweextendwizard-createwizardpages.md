---
UID: NF:cluadmex.IWEExtendWizard.CreateWizardPages
title: IWEExtendWizard::CreateWizardPages
author: windows-sdk-content
description: Allows you to create wizard pages and add them to Failover Cluster Administrator's New Resource Wizard or Cluster Application Wizard.
old-location: mscs\iweextendwizard_createwizardpages.htm
tech.root: mscs
ms.assetid: b52ea5a5-aa80-4f65-9bab-b60fa8363b01
ms.author: windowssdkdev
ms.date: 10/24/2018
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
 - IWEExtendWizard.CreateWizardPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWEExtendWizard::CreateWizardPages


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create wizard pages and add them to 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator's</a> New Resource Wizard 
     or Cluster Application Wizard.


## -parameters




### -param piData [in]


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer for retrieving information 
       relating to the wizard pages to be added. By calling 
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
Depending on the type of <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a> for 
       which the wizard page is being created, a pointer to one of the following interfaces is also available:

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

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa370517(v=VS.85).aspx">IWCWizardCallback</a> interface 
       implementation used to add the new property pages to the wizard.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks



To add Wizard97 wizard pages, use the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a> 
     method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>For each property page to be added</b>

<ol>
<li>Use <i>piData</i> to call 
       <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> and retrieve an interface 
       pointer for the <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster object</a> associated with the new 
       page. For example, if you are adding a property page for a resource, you want to retrieve a pointer to the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the object being 
       extended, you should expect to receive errors when you attempt to call the methods.</li>
<li>
To create the page, call the function 
       <a href="https://msdn.microsoft.com/en-us/library/Bb760807(v=VS.85).aspx">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new property page should be no larger than 252 
       dialog units wide and 218 dialog units high, and should contain two standard controls:

<ul>
<li>For the object icon, an icon control positioned at (8,7) with a size of (18,20).</li>
<li>For the object name, a static control positioned at (38,12) with a size of (247,10).</li>
</ul>
</li>
<li>To add the page to a Cluster Administrator Wizard, call 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370521(v=VS.85).aspx">IWCWizardCallback::AddWizardPage</a> 
       using the <i>piCallback</i> pointer.</li>
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



<a href="https://msdn.microsoft.com/en-us/library/Aa370509(v=VS.85).aspx">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370517(v=VS.85).aspx">IWCWizardCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370724(v=VS.85).aspx">IWEExtendWizard</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370728(v=VS.85).aspx">IWEExtendWizard97</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a>
 

 

