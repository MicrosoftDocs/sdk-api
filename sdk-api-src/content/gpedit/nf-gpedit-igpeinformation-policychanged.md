---
UID: NF:gpedit.IGPEInformation.PolicyChanged
title: IGPEInformation::PolicyChanged (gpedit.h)
description: The PolicyChanged method informs the Group Policy Object Editor that policy settings have changed.
helpviewer_keywords: ["IGPEInformation interface [Group Policy]","PolicyChanged method","IGPEInformation.PolicyChanged","IGPEInformation::PolicyChanged","PolicyChanged","PolicyChanged method [Group Policy]","PolicyChanged method [Group Policy]","IGPEInformation interface","_win32_igpeinformation_policychanged","gpedit/IGPEInformation::PolicyChanged","policy.igpeinformation_policychanged"]
old-location: policy\igpeinformation_policychanged.htm
tech.root: Policy
ms.assetid: 4c36fbcb-2adb-4c32-87d3-efcd55dbaf3e
ms.date: 12/05/2018
ms.keywords: IGPEInformation interface [Group Policy],PolicyChanged method, IGPEInformation.PolicyChanged, IGPEInformation::PolicyChanged, PolicyChanged, PolicyChanged method [Group Policy], PolicyChanged method [Group Policy],IGPEInformation interface, _win32_igpeinformation_policychanged, gpedit/IGPEInformation::PolicyChanged, policy.igpeinformation_policychanged
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
req.lib: 
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPEInformation::PolicyChanged
 - gpedit/IGPEInformation::PolicyChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation.PolicyChanged
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
    write an MMC snap-in you must implement the <a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> 
    interface and call the <a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify">IComponentData::Notify</a> 
    method. To get the <a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a> interface, set the 
    <i>event</i> parameter of the 
    <b>IComponentData::Notify</b> method to be 
    <b>MMCN_EXPAND</b> and the <i>arg</i> parameter to 
    <b>TRUE</b>. You can then obtain the 
    <b>IGPEInformation</b> interface by calling 
    <b>QueryInterface</b> and by using the usual Rules for Implementing QueryInterface.

For example, you can obtain the interface by calling as follows.


```cpp
lpDataObject->QueryInterface(IID_IGPEInformation, (LPVOID lpDataObject->*)&m_pGPTInformation);
```

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>