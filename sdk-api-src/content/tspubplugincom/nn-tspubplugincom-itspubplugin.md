---
UID: NN:tspubplugincom.ItsPubPlugin
title: ItsPubPlugin
author: windows-driver-content
description: Exposes properties and methods that provide information about resources available to users of RemoteApp and Desktop Connections.
old-location: termserv\itspubplugin.htm
old-project: TermServ
ms.assetid: 37d33f27-a811-4c97-bc80-ff8a5b8fcb7c
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ItsPubPlugin, ItsPubPlugin interface [Remote Desktop Services], ItsPubPlugin interface [Remote Desktop Services],described, termserv.itspubplugin, tspubplugincom/ItsPubPlugin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tspubplugincom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Cpubplugin.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: pluginResource2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tspubplugincom.h
api_name:
-	ItsPubPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ItsPubPlugin interface


## -description


Exposes properties and methods that provide information about resources available to users of RemoteApp and Desktop Connections. The methods in this interface are called by the RemoteApp and Desktop Connection Management service in Remote Desktop Web Access (RD Web Access) and Remote Desktop Connection Broker (RD Connection Broker).

Resources that can be exposed through <b>ItsPubPlugin</b> typically include RemoteApp programs, virtual machine pools, and personal virtual desktops. By implementing this interface and registering it in the Registry, these resources can be displayed to users in RD Web Access and RemoteApp and Desktop Connections.  Your interface can perform custom filtering of resources and provide support for file types that are not currently supported. (Only .rdp files are supported by default.) 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ItsPubPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ItsPubPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ItsPubPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66b18c7f-2623-44ed-8cb9-3cceaa9bab34">GetCacheLastUpdateTime</a>
</td>
<td align="left" width="63%">
Returns the time that the cache was last updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eceadfef-6980-452a-b983-3813f6e7ade8">GetResource</a>
</td>
<td align="left" width="63%">
This method is reserved and should always return <b>E_NOTIMPL</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8f255fe-6f31-4cbb-a600-a27e977a84a0">GetResourceList</a>
</td>
<td align="left" width="63%">
Retrieves a list of resources assigned to the specified user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/035b9d13-b64e-4e1c-8623-b4456f36c4ee">ResolveResource</a>
</td>
<td align="left" width="63%">
 Provides information about how to connect to a user's assigned personal virtual desktop. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ItsPubPlugin</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c1ea46b6-fac6-4140-a278-cb04ee9af739">pluginName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the  name of the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/39e5cc01-3945-4e78-bbce-bff5d5a5f22d">pluginVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the version of the plug-in.

</td>
</tr>
</table> 


## -remarks



<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To register your plug-in so that it will be called by the RemoteApp and Desktop Connection Management service</b>

<ol>
<li>Implement the plug-in in a DLL and register the DLL by using the Regsvr32.exe tool.</li>
<li>Create a subkey named for the CLSID of the DLL under the following key:<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>Terminal Server</b>
                  <b>CentralizedPublishing</b>
                     <b>Plugins</b></pre>
</li>
<li>Create a value for the subkey of type <b>DWORD</b> with the name "IsEnabled". To allow the service to call the plug-in, set the value to one. To disallow calls to the plug-in, set the value to zero. You do not need to restart the service because the service loads the plug-in automatically.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/bd928bdc-e4b4-4b5a-a782-0881ed6d08bd">RemoteApp and Desktop Connection Management Service Interfaces</a>



<a href="https://msdn.microsoft.com/4295bd3c-0fc9-4135-b9cc-cafbc8381797">RemoteApp and Desktop Connection Management Service Structures</a>
 

 

