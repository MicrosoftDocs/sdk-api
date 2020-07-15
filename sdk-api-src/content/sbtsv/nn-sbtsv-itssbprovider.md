---
UID: NN:sbtsv.ITsSbProvider
title: ITsSbProvider (sbtsv.h)
description: Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.
helpviewer_keywords: ["ITsSbProvider","ITsSbProvider interface [Remote Desktop Services]","ITsSbProvider interface [Remote Desktop Services]","described","sbtsv/ITsSbProvider","termserv.itssbprovider"]
old-location: termserv\itssbprovider.htm
tech.root: TermServ
ms.assetid: a8574750-d86e-4b0d-a534-d005596e2a33
ms.date: 12/05/2018
ms.keywords: ITsSbProvider, ITsSbProvider interface [Remote Desktop Services], ITsSbProvider interface [Remote Desktop Services],described, sbtsv/ITsSbProvider, termserv.itssbprovider
f1_keywords:
- sbtsv/ITsSbProvider
dev_langs:
- c++
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
- sbtsv.h
api_name:
- ITsSbProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbProvider interface


## -description


Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.

The  <b>ITsSbProvider</b> interface is a helper interface, aimed at reducing the amount of code that the plug-in 
implementer needs to write. It provides a default implementation of some objects, such as 
environment, target, and session objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createenvironmentobject">CreateEnvironmentObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment">ITsSbEnvironment</a> environment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createenvironmentpropertysetobject">CreateEnvironmentPropertySetObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset">ITsSbEnvironmentPropertySet</a> environment property set object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createloadbalanceresultobject">CreateLoadBalanceResultObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult">ITsSbLoadBalanceResult</a> load-balancing result 
object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createpluginpropertyset">CreatePluginPropertySet</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginpropertyset">ITsSbPluginPropertySet</a> plug-in property set object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createsessionobject">CreateSessionObject</a>
</td>
<td align="left" width="63%">
Plug-ins can use the <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createsessionobject">CreateSessionObject</a> method to create an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a> session object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createtargetobject">CreateTargetObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> target object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-createtargetpropertysetobject">CreateTargetPropertySetObject</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtargetpropertyset">ITsSbTargetPropertySet</a> target property set object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-getfilterpluginstore">GetFilterPluginStore</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore">FilterPluginStore</a> instance of the  filter plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-getinstanceofglobalstore">GetInstanceOfGlobalStore</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a> instance of the global store object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-getresourcepluginstore">GetResourcePluginStore</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a> instance of the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-registerfornotification">RegisterForNotification</a>
</td>
<td align="left" width="63%">
Requests that  RD Connection Broker send notifications about specified events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovider-unregisterfornotification">UnRegisterForNotification</a>
</td>
<td align="left" width="63%">
Requests that  RD Connection Broker not send notifications about specified events.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

