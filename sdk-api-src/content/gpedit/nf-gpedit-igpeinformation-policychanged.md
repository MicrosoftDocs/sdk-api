---
UID: NF:gpedit.IGPEInformation.PolicyChanged
title: IGPEInformation::PolicyChanged
author: windows-driver-content
description: The PolicyChanged method informs the Group Policy Object Editor that policy settings have changed.
old-location: policy\igpeinformation_policychanged.htm
old-project: Policy
ms.assetid: 4c36fbcb-2adb-4c32-87d3-efcd55dbaf3e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IGPEInformation interface [Group Policy],PolicyChanged method, IGPEInformation.PolicyChanged, IGPEInformation::PolicyChanged, PolicyChanged, PolicyChanged method [Group Policy], PolicyChanged method [Group Policy],IGPEInformation interface, _win32_igpeinformation_policychanged, gpedit/IGPEInformation::PolicyChanged, policy.igpeinformation_policychanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IGPEInformation.PolicyChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPEInformation::PolicyChanged


## -description


The <b>PolicyChanged</b> method informs the 
    Group Policy Object Editor that policy settings have changed.


## -parameters




### -param bMachine [in]

Specifies whether computer or user policy has changed. If this value is <b>TRUE</b>, 
      computer policy has changed. If this value is <b>FALSE</b>, user policy has changed.


### -param bAdd [in]

Specifies whether this is an add or delete operation. If this parameter is <b>FALSE</b>, 
      the last policy setting for the specified extension <i>pGuidExtension</i> is removed. In all 
      other cases, this parameter is <b>TRUE</b>.


### -param pGuidExtension [in]

Pointer to the <b>GUID</b> or unique name of the snap-in extension that will process 
      policy. If the GPO is to be processed by the snap-in that processes .pol files, this parameter must specify the 
      <b>REGISTRY_EXTENSION_GUID</b> value.


### -param pGuidSnapin [in]

Pointer to the GUID or unique name of the snap-in extension making this method call.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes 
       defined in the Platform SDK header file WinError.h.




## -remarks



An extension must call this method every time it makes a change to a group policy object. Note that when you 
    write an MMC snap-in you must implement the <a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> 
    interface and call the <a href="https://msdn.microsoft.com/8679396e-23d0-4418-987a-c72b1508e7b9">IComponentData::Notify</a> 
    method. To get the <a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a> interface, set the 
    <i>event</i> parameter of the 
    <b>IComponentData::Notify</b> method to be 
    <b>MMCN_EXPAND</b> and the <i>arg</i> parameter to 
    <b>TRUE</b>. You can then obtain the 
    <b>IGPEInformation</b> interface by calling 
    <b>QueryInterface</b> and by using the usual Rules for Implementing QueryInterface.

For example, you can obtain the interface by calling as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>lpDataObject-&gt;QueryInterface(IID_IGPEInformation, (LPVOID lpDataObject-&gt;*)&amp;m_pGPTInformation);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>



<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a>
 

 

