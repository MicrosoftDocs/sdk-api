---
UID: NF:mmc.ISnapinHelp.GetHelpTopic
title: ISnapinHelp::GetHelpTopic (mmc.h)
description: Enables a snap-in to add its compiled HTML Help file to the MMC Help collection file.
helpviewer_keywords: ["GetHelpTopic","GetHelpTopic method [MMC]","GetHelpTopic method [MMC]","ISnapinHelp interface","ISnapinHelp interface [MMC]","GetHelpTopic method","ISnapinHelp.GetHelpTopic","ISnapinHelp::GetHelpTopic","mmc.isnapinhelp_gethelptopic","mmc/ISnapinHelp::GetHelpTopic"]
old-location: mmc\isnapinhelp_gethelptopic.htm
tech.root: mmc
ms.assetid: 2F7E987F-1E1E-4C9E-9B26-D7BB8F5A05DD
ms.date: 12/05/2018
ms.keywords: GetHelpTopic, GetHelpTopic method [MMC], GetHelpTopic method [MMC],ISnapinHelp interface, ISnapinHelp interface [MMC],GetHelpTopic method, ISnapinHelp.GetHelpTopic, ISnapinHelp::GetHelpTopic, mmc.isnapinhelp_gethelptopic, mmc/ISnapinHelp::GetHelpTopic
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
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
 - ISnapinHelp::GetHelpTopic
 - mmc/ISnapinHelp::GetHelpTopic
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
 - ISnapinHelp.GetHelpTopic
---

# ISnapinHelp::GetHelpTopic


## -description

Enables a snap-in to add its compiled HTML Help file to the MMC Help collection file.

## -parameters

### -param lpCompiledHelpFile [out]

A pointer to the address of the null-terminated Unicode string that contains the path of the compiled Help file (.chm) for the snap-in. When specifying the path, place the file anywhere and specify the full path name.

## -returns

This method can return one of these values.

## -remarks

MMC calls the snap-in's implementation of this method to get the location of the snap-in's Help file. MMC merges the HTML Help files of all snap-ins with the MMC console HTML Help collection file.

The topic hierarchy from the snap-in's Help file will appear in the table of contents when the collection is viewed.

By merging the HTML Help files, MMC creates a single, integrated HTML Help table of contents, index, and search feature. When a user clicks Help on Microsoft Management Console on the main 
<b>Help</b> menu, MMC opens the merged Help file that includes HTML Help files for all snap-ins in the current console file.

Allocate the <i>lpCompiledHelpFile</i> string with the COM API function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release it.


#### Examples


```cpp
STDMETHODIMP CComponentData::GetHelpTopic( LPOLESTR *lpCompiledFile )
{
    LPOLESTR lpHelpFile;
 
    if ( !lpCompiledFile )
        return E_POINTER; // invalid argument
 
    lpHelpFile = (LPOLESTR) CoTaskMemAlloc( MAX_PATH * sizeof(WCHAR) );
 
    if ( !lpHelpFile )
    {
        return E_OUTOFMEMORY;
    }
 
    ExpandEnvironmentStringsW( L"%SystemRoot%\\Help\\myhelpfile.chm", lpHelpFile, MAX_PATH );
 
    *lpCompiledHelpFile = lpHelpFile;
 
    return S_OK;
}
```

## -see-also

<a href="/previous-versions/windows/desktop/mmc/adding-html-help-support">Adding HTML Help Support</a>



<a href="/windows/desktop/api/mmc/nf-mmc-idisplayhelp-showtopic">IDisplayHelp::ShowTopic</a>



<a href="/windows/desktop/api/mmc/nn-mmc-isnapinhelp">ISnapinHelp</a>



<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertyhelp">MMCPropertyHelp</a>



<a href="/previous-versions/windows/desktop/mmc/providing-mui-compliant-help-files">Providing MUI-Compliant Help Files</a>