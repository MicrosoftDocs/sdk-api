---
UID: NF:mmc.IDisplayHelp.ShowTopic
title: IDisplayHelp::ShowTopic (mmc.h)
description: The IDisplayHelp::ShowTopic method displays the specified HTML Help topic in the merged MMC HTML Help file.
helpviewer_keywords: ["IDisplayHelp interface [MMC]","ShowTopic method","IDisplayHelp.ShowTopic","IDisplayHelp::ShowTopic","ShowTopic","ShowTopic method [MMC]","ShowTopic method [MMC]","IDisplayHelp interface","_slate_idisplayhelp_showtopic","mmc.idisplayhelp_showtopic","mmc/IDisplayHelp::ShowTopic"]
old-location: mmc\idisplayhelp_showtopic.htm
tech.root: mmc
ms.assetid: 184adc09-8b48-4a2e-bbd9-ec6bd9085c32
ms.date: 12/05/2018
ms.keywords: IDisplayHelp interface [MMC],ShowTopic method, IDisplayHelp.ShowTopic, IDisplayHelp::ShowTopic, ShowTopic, ShowTopic method [MMC], ShowTopic method [MMC],IDisplayHelp interface, _slate_idisplayhelp_showtopic, mmc.idisplayhelp_showtopic, mmc/IDisplayHelp::ShowTopic
req.header: mmc.h
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDisplayHelp::ShowTopic
 - mmc/IDisplayHelp::ShowTopic
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IDisplayHelp.ShowTopic
---

# IDisplayHelp::ShowTopic


## -description

The <b>IDisplayHelp::ShowTopic</b> method displays the specified HTML Help topic in the merged MMC HTML Help file.

## -parameters

### -param pszHelpTopic [in]

A pointer to a <b>NULL</b>-terminated string specifying the topic to display in the merged MMC HTML Help file. The string must have the following format:


```cpp
helpfilename::topicfilename
```


where <i>helpfilename</i> is the file name of the snap-in's HTML Help file (.chm) that MMC merged into the MMC HTML Help collection file (this is the file name only, not the path to the original HTML Help file), and <i>topicfilename</i> is the internal path to the topic file within the snap-in's .chm file. The author of the snap-in's HTML Help file determines whether there is an internal directory structure for the topic HTML files or if all topic HTML files are at the root of the .chm file.

A snap-in tells MMC about its .chm file in its implementation of the 
<a href="/previous-versions/windows/desktop/legacy/aa814944(v=vs.85)">ISnapinHelp2::GetHelpTopic</a> method.

For example, if the snap-in had the HTML Help file mysnapin.chm merged into the MMC HTML Help collection file, and a topic HTML file that had the internal file path of htm/help01.htm, the string would have the following form:


```cpp
mysnapin.chm::htm/help01.htm
```


If instead the help01.htm topic file is at the root of the mysnapin.chm Help file, the string should have the following form:


```cpp
mysnapin.chm::/help01.htm
```


Support for numeric IDs for topics is not included in versions 1.2 and earlier.

## -returns

This method can return one of these values.

## -remarks

MMC versions 1.0 and 1.1 required that <i>pszHelpTopic</i> be allocated with the COM API function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and that MMC would then free the string. This violated the COM rules for allocation of in-parameters, which require that they be both allocated and freed by the caller (the snap-in). In MMC 1.2 and MMC 2.0, it is no longer required that <i>pszHelpTopic</i> be allocated with <b>CoTaskMemAlloc</b>. The caller is free to use whatever memory management it desires. If the caller chooses to use <b>CoTaskMemAlloc</b>, it is also responsible for calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free the string.

A snap-in can provide context help for the selected item by handling the <a href="/previous-versions/windows/desktop/mmc/mmcn-contexthelp">MMCN_CONTEXTHELP</a> notification in its 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a> method and calling <b>IDisplayHelp::ShowTopic</b>.

For property pages, the snap-in should call 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertyhelp">MMCPropertyHelp</a> instead of <b>IDisplayHelp::ShowTopic</b>. Because an MMC property sheet is typically running on a separate thread, the property page cannot use the 
<a href="/windows/desktop/api/mmc/nn-mmc-idisplayhelp">IDisplayHelp</a> interface directly. Instead, the property page can call 
<b>MMCPropertyHelp</b> from the MMC library to achieve the same result. 
<b>MMCPropertyHelp</b> takes the same topic string parameter as <b>IDisplayHelp::ShowTopic</b> and handles marshalling the request to the main MMC thread.

If the snap-in handles the <a href="/previous-versions/windows/desktop/mmc/mmcn-contexthelp">MMCN_CONTEXTHELP</a> notification, MMC expects the snap-in to specify a Help topic for the selected item. Consequently, in the notification handler for the <b>MMCN_CONTEXTHELP</b> notification, the snap-in has two options:

<ul>
<li>It can call <b>IDisplayHelp::ShowTopic</b> or 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertyhelp">MMCPropertyHelp</a> to specify the Help topic and then return <b>S_OK</b> to indicate success. Be aware that the snap-in should only return <b>S_OK</b> if it specifies a Help topic. If the snap-in returns <b>S_OK</b> without specifying a Help topic, no Help topic will be displayed.</li>
<li>It can return <b>S_FALSE</b> to the notification. MMC then displays the Help collection file with the default MMC topic selected.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa814944(v=vs.85)">ISnapinHelp2::GetHelpTopic</a>



<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertyhelp">MMCPropertyHelp</a>