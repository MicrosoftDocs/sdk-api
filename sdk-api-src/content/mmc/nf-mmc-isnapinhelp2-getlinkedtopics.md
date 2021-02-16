---
UID: NF:mmc.ISnapinHelp2.GetLinkedTopics
title: ISnapinHelp2::GetLinkedTopics (mmc.h)
description: Enables a snap-in to specify the names and locations of any HTML Help files that are linked to the snap-in's Help file (specified in the GetHelpTopic method).
helpviewer_keywords: ["GetLinkedTopics","GetLinkedTopics method [MMC]","GetLinkedTopics method [MMC]","ISnapinHelp2 interface","ISnapinHelp2 interface [MMC]","GetLinkedTopics method","ISnapinHelp2.GetLinkedTopics","ISnapinHelp2::GetLinkedTopics","_slate_isnapinhelp2_getlinkedtopics","mmc.isnapinhelp2_getlinkedtopics","mmc/ISnapinHelp2::GetLinkedTopics"]
old-location: mmc\isnapinhelp2_getlinkedtopics.htm
tech.root: mmc
ms.assetid: ceed0d9f-e1bf-4692-aadf-e924095cdfc8
ms.date: 12/05/2018
ms.keywords: GetLinkedTopics, GetLinkedTopics method [MMC], GetLinkedTopics method [MMC],ISnapinHelp2 interface, ISnapinHelp2 interface [MMC],GetLinkedTopics method, ISnapinHelp2.GetLinkedTopics, ISnapinHelp2::GetLinkedTopics, _slate_isnapinhelp2_getlinkedtopics, mmc.isnapinhelp2_getlinkedtopics, mmc/ISnapinHelp2::GetLinkedTopics
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
 - ISnapinHelp2::GetLinkedTopics
 - mmc/ISnapinHelp2::GetLinkedTopics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinHelp2.GetLinkedTopics
---

# ISnapinHelp2::GetLinkedTopics


## -description

The <b>ISnapinHelp2::GetLinkedTopics</b> method enables a snap-in to specify the names and locations of any HTML Help files that are linked to the snap-in's Help file (specified in the 
<a href="/windows/desktop/api/mmc/nf-mmc-isnapinhelp-gethelptopic">GetHelpTopic</a> method).

## -parameters

### -param lpCompiledHelpFiles [out]

A pointer to the address of the null-terminated Unicode string that contains the path of one or more compiled Help files (.chm) that are linked to the snap-in's Help file. A semicolon is used to separate multiple file paths from each other.

When specifying the path, place the file anywhere and specify the full path name.

## -returns

This method can return one of these values.

## -remarks

MMC calls the snap-in's <b>ISnapinHelp2::GetLinkedTopics</b> method only if the snap-in returned <b>S_OK</b> from the 
<a href="/previous-versions/windows/desktop/legacy/aa814944(v=vs.85)">ISnapinHelp2::GetHelpTopic</a> method call.

Allocate the <i>lpCompiledHelpFiles</i> string with the COM API function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release it

## -see-also

<a href="/previous-versions/windows/desktop/mmc/adding-html-help-support">Adding HTML Help Support</a>



<a href="/windows/desktop/api/mmc/nn-mmc-isnapinhelp2">ISnapinHelp2</a>



<a href="/previous-versions/windows/desktop/legacy/aa814944(v=vs.85)">ISnapinHelp2::GetHelpTopic</a>