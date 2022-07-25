---
UID: NN:shappmgr.IAppPublisher
title: IAppPublisher (shappmgr.h)
description: Exposes methods for publishing applications through Add/Remove Programs in Control Panel. This is the principal interface implemented for this purpose.
helpviewer_keywords: ["IAppPublisher","IAppPublisher interface [Windows Shell]","IAppPublisher interface [Windows Shell]","described","inet_IAppPublisher","shappmgr/IAppPublisher","shell.IAppPublisher"]
old-location: shell\IAppPublisher.htm
tech.root: shell
ms.assetid: 5391444a-53b6-48c9-9a94-d045b3f97182
ms.date: 12/05/2018
ms.keywords: IAppPublisher, IAppPublisher interface [Windows Shell], IAppPublisher interface [Windows Shell],described, inet_IAppPublisher, shappmgr/IAppPublisher, shell.IAppPublisher
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - IAppPublisher
 - shappmgr/IAppPublisher
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IAppPublisher
---

# IAppPublisher interface


## -description

Exposes methods for publishing applications through <b>Add/Remove Programs</b> in Control Panel. This is the principal interface implemented for this purpose.

## -inheritance

The <b>IAppPublisher</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppPublisher</b> also has these types of members:

## -remarks

<b>Add/Remove Programs</b> in Control Panel creates a registered publisher object and requests its <b>IAppPublisher</b> interface.  You can create published application objects using the application enumerator, which you create using <b>IAppPublisher</b>.

<b>Add/Remove Programs</b> gathers a list of published applications from publishers and then uses a publisher to display these applications with Microsoft Active Directory.  When the user clicks <b>Add New Programs</b> in <b>Add/Remove Programs,</b> a list of published applications appears.

You can publish applications in <b>Add/Remove Programs </b> using the following Component Object Model (COM) interfaces.

<ul>
<li><b>IAppPublisher</b></li>
<li>
<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>
</li>
<li>
<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>
</li>
</ul>
When you implement these interfaces, you must register your COM object in the registry.  To register your publisher, add your object's class identifier (CLSID) under the following registry key.


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>AppManagement</b>
                  <b>Publishers</b></pre>


For example, if your publisher is named "My Publisher", you  create a new key under "Publishers" named "My Publisher" with its default REG_SZ value as the publisher's CLSID:


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>AppManagement</b>
                  <b>Publishers</b>
                     <b>My Publisher</b>
                        (Default) = {4D05CD3D-FFED-46bb-B9F1-321C26BE6362}</pre>


You can also create the typical COM server registration entries as follows:


<pre><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <b>{469EE8CE-1B86-4524-9042-AAA44FD9C8F2}</b>
         (Default) = Sample Applications Publisher
         <b>InProcServer32</b>
            (Default) = pubdemo.dll
            <b>ThreadingModel</b> = Apartment</pre>


With the publisher registered in this way, <b>Add/Remove Programs</b> creates an instance of your object by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> for your object and requesting the appropriate <b>IAppPublisher</b> interface when the <b>Add New Programs</b> view is populated. Using <b>IAppPublisher</b>, Add/Remove Programs retrieves the application enumerator (<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>) and information that describes the published applications.  Your implementation of <a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> is responsible for installing the associated application in its <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-install">IPublishedApp::Install</a> method. Add/Remove Programs calls this method when the user clicks the <b>Add</b> or the <b>Add Later</b> button in the user interface.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ienumpublishedapps">IEnumPublishedApps</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>
