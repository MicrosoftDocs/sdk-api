---
UID: NN:sbtsv.ITsSbPlugin
title: ITsSbPlugin (sbtsv.h)
description: Exposes methods that initialize and terminate plug-ins.
helpviewer_keywords: ["ITsSbPlugin","ITsSbPlugin interface [Remote Desktop Services]","ITsSbPlugin interface [Remote Desktop Services]","described","sbtsv/ITsSbPlugin","termserv.itssbplugin"]
old-location: termserv\itssbplugin.htm
tech.root: TermServ
ms.assetid: db3d3ee7-9e53-4bac-9711-4e85f1016db9
ms.date: 12/05/2018
ms.keywords: ITsSbPlugin, ITsSbPlugin interface [Remote Desktop Services], ITsSbPlugin interface [Remote Desktop Services],described, sbtsv/ITsSbPlugin, termserv.itssbplugin
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbPlugin
 - sbtsv/ITsSbPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbPlugin
---

# ITsSbPlugin interface


## -description

Exposes methods that initialize and terminate plug-ins.

This is the base interface for all plug-ins to Remote Desktop Connection Broker (RD Connection Broker). Derive from this interface to 
    create plug-ins for load balancing, placement, or orchestration.

## -inheritance

The <b>ITsSbPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbPlugin</b> also has these types of members:

## -remarks

Two different types of plugins are supported - filters and resources. Resource plugins are for supporting new 
     types of resources (for example VMs running on different hypervisors). Filter plugins allow the plugins to change 
     the information passed to other plugins (for example passing resource requests to the least utilized node.)

To register a resource filter, add these values to the registry.


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SYSTEM</b>
      <b>CurrentControlSet</b>
         <b>Services</b>
            <b>Tssdis</b>
               <b>Parameters</b>
                  <b>Plugins</b>
                     <b>Resource</b>
                        <i>YOUR_RESOURCE_PLUGIN_NAME</i>
                           <b>CLSID</b> = {<i>CLSID of your resource provider</i>}<dl>
<dt>                           Data type</dt>
<dd>                           REG_SZ</dd>
</dl>
                           <b>Provider</b> = <i>Name_of_resource_provider</i><dl>
<dt>                           Data type</dt>
<dd>                           REG_SZ</dd>
</dl>
                           <b>IsEnabled</b> = 1<dl>
<dt>                           Data type</dt>
<dd>                           REG_DWORD</dd>
</dl>
</pre>


The names used should be unique and identify the company, product, and/or feature. They are not shown to the user 
     but can be seen in some logs.

 

To register a filter provider, add these values to the registry.


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SYSTEM</b>
      <b>CurrentControlSet</b>
         <b>Services</b>
            <b>Tssdis</b>
               <b>Parameters</b>
                  <b>Plugins</b>
                     <b>Filter</b>
                        <i>1</i>
                           <b>CLSID</b> = {<i>CLSID of filter provider 1</i>}<dl>
<dt>                           Data type</dt>
<dd>                           REG_SZ</dd>
</dl>
                           <b>Provider</b> = <i>Name of filter provider 1</i><dl>
<dt>                           Data type</dt>
<dd>                           REG_SZ</dd>
</dl>
                           <b>IsEnabled</b> = 1<dl>
<dt>                           Data type</dt>
<dd>                           REG_DWORD</dd>
</dl>
                        <i>2…</i>
                           <b>CLSID</b> = {<i>CLSID of filter provider 2</i>}<dl>
<dt>                           Data type</dt>
<dd>                           REG_SZ</dd>
</dl>
                           <b>Provider</b> = <i>Name of filter provider 2</i><dl>
<dt>                           Data type</dt>
<dd>                           REG_SZ</dd>
</dl>
                           <b>IsEnabled</b> = 1<dl>
<dt>                           Data type</dt>
<dd>                           REG_DWORD</dd>
</dl>
</pre>


First the system will load Filter 1, then load Filter 2, etc..

## -see-also

<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
