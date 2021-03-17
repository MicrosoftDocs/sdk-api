---
UID: NF:mmc.MMCPropertyHelp
title: MMCPropertyHelp function (mmc.h)
description: Displays the specified HTML Help topic in the merged MMC HTML Help file for a property page.
helpviewer_keywords: ["MMCPropertyHelp","MMCPropertyHelp callback","MMCPropertyHelp callback function [MMC]","_slate_mmcpropertyhelp","mmc.mmcpropertyhelp","mmc/MMCPropertyHelp"]
old-location: mmc\mmcpropertyhelp.htm
tech.root: mmc
ms.assetid: c3b0fa86-dff4-4c35-9b08-633448db18be
ms.date: 12/05/2018
ms.keywords: MMCPropertyHelp, MMCPropertyHelp callback, MMCPropertyHelp callback function [MMC], _slate_mmcpropertyhelp, mmc.mmcpropertyhelp, mmc/MMCPropertyHelp
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MMCPropertyHelp
 - mmc/MMCPropertyHelp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mmc.h
api_name:
 - MMCPropertyHelp
---

# MMCPropertyHelp function


## -description

The MMCPropertyHelp function is introduced in MMC 1.1.

The MMCPropertyHelp function displays the specified HTML Help topic in the merged MMC HTML Help file for a property page.

## -parameters

### -param pszHelpTopic

A pointer to a NULL-terminated string specifying the topic to display in the merged MMC HTML Help file. The string must have the following format:

<i>helpfilename</i>::<i>topicfilename</i>

where <i>helpfilename</i> is the file name of the snap-in's HTML Help file (.chm) that MMC merged into the MMC HTML Help file (file name only, not the path to the original HTML Help file) and <i>topicfilename</i> is the internal path to the topic file within the snap-in's .chm file. The author of the snap-in's HTML Help file determines whether there is an internal directory structure for the topic HTML files or if all topic HTML files are at the root of the .chm file.

For example, if the snap-in had the HTML Help file mysnapin.chm merged into the MMC HTML Help file and a topic HTML file that had the internal Help file path of htm/snphlp01.htm, the string would have the following form:

mysnapin.chm::htm/snphlp01.htm

Support for numeric IDs for topics is not available in this release.

## -returns

This callback function can return one of these values.

## -remarks

Call 
MMCPropertyHelp in the notification handler for the 
<a href="/previous-versions/windows/desktop/mmc/mmcn-contexthelp">MMCN_CONTEXTHELP</a> notification.

A snap-in can provide context help on a property page. Because an MMC property sheet is typically running on a separate thread, the property page cannot use the 
<a href="/windows/desktop/api/mmc/nn-mmc-idisplayhelp">IDisplayHelp</a> interface directly. Instead, the property page can call 
MMCPropertyHelp from the MMC library to achieve the same result. 
MMCPropertyHelp takes the same topic string parameter as 
<a href="/windows/desktop/api/mmc/nf-mmc-idisplayhelp-showtopic">IDisplayHelp::ShowTopic</a> and handles marshaling the request to the main MMC thread.

If the snap-in handles the <a href="/previous-versions/windows/desktop/mmc/mmcn-contexthelp">MMCN_CONTEXTHELP</a> notification, MMC expects the snap-in to specify a Help topic for the selected item. Consequently, in the notification handler for the <b>MMCN_CONTEXTHELP</b> notification, the snap-in has two options:

<ul>
<li>It can call <a href="/windows/desktop/api/mmc/nf-mmc-idisplayhelp-showtopic">IDisplayHelp::ShowTopic</a> or 
<i>MMCPropertyHelp</i> to specify the Help topic and then return <b>S_OK</b> to indicate success. Be aware that the snap-in should only return <b>S_OK</b> if it specifies a Help topic. If the snap-in returns <b>S_OK</b> without specifying a Help topic, no Help topic will be displayed.</li>
<li>It can return S_FALSE to the notification. MMC then brings up the table of contents with the default MMC topic selected.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-idisplayhelp-showtopic">IDisplayHelp::ShowTopic</a>



<a href="/previous-versions/windows/desktop/legacy/aa814944(v=vs.85)">ISnapinHelp2::GetHelpTopic</a>