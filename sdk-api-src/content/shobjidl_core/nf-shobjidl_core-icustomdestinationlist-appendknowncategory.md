---
UID: NF:shobjidl_core.ICustomDestinationList.AppendKnownCategory
title: ICustomDestinationList::AppendKnownCategory (shobjidl_core.h)
description: Specifies that the Frequent or Recent category should be included in a custom Jump List.
helpviewer_keywords: ["AppendKnownCategory","AppendKnownCategory method [Windows Shell]","AppendKnownCategory method [Windows Shell]","ICustomDestinationList interface","ICustomDestinationList interface [Windows Shell]","AppendKnownCategory method","ICustomDestinationList.AppendKnownCategory","ICustomDestinationList::AppendKnownCategory","KDC_FREQUENT","KDC_RECENT","_shell_ICustomDestinationList_AppendKnownCategory","shell.ICustomDestinationList_AppendKnownCategory","shobjidl_core/ICustomDestinationList::AppendKnownCategory"]
old-location: shell\ICustomDestinationList_AppendKnownCategory.htm
tech.root: shell
ms.assetid: ce73fff3-8d1a-4912-98ce-7149460ffa49
ms.date: 12/05/2018
ms.keywords: AppendKnownCategory, AppendKnownCategory method [Windows Shell], AppendKnownCategory method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],AppendKnownCategory method, ICustomDestinationList.AppendKnownCategory, ICustomDestinationList::AppendKnownCategory, KDC_FREQUENT, KDC_RECENT, _shell_ICustomDestinationList_AppendKnownCategory, shell.ICustomDestinationList_AppendKnownCategory, shobjidl_core/ICustomDestinationList::AppendKnownCategory
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICustomDestinationList::AppendKnownCategory
 - shobjidl_core/ICustomDestinationList::AppendKnownCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICustomDestinationList.AppendKnownCategory
---

# ICustomDestinationList::AppendKnownCategory


## -description

Specifies that the <b>Frequent</b> or <b>Recent</b> category should be included in a custom Jump List.

## -parameters

### -param category [in]

Type: <b>KNOWNDESTCATEGORY</b>

One of the following values that indicate which known category to add to the list:

#### KDC_FREQUENT (1)

1 - Add the <b>Frequent</b> category.

#### KDC_RECENT (2)

2 - Add the <b>Recent</b> category.

#### KDC_NONE (-1)

-1 - Do not use a category. Note, this value is not represented in KNOWNDESTCATEGORY, use `static_cast<KNOWNDESTCATEGORY>(-1)` to represent this.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. 
                
                    

If there is a privacy Group Policy or user privacy setting present, it can affect the result of this method. Categories that contain user-specific items based on individual usage are not allowed under those privacy settings. Due to this, the <b>Recent</b> or <b>Frequent</b> categories added through this method will have no data, and categories with no data are not displayed. However, in that situation, this method call will not result in a failure code.

## -remarks

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> before you call this method.

The <b>Recent</b> category is shown in a default Jump List, but to show it in a custom Jump List together with custom categories you must explicitly request it through this method.

With both <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">AppendCategory</a> and <b>AppendKnownCategory</b>, a custom Jump List should be designed to avoid any item appearing in more than one category. If two categories are simply different views on the same data, one of those categories should be removed since it is using Jump List space without contributing to the user's convenience. Duplicates are not hidden by the system except in the case of a pinned destination, in which case that destination is shown in the Pinned category and hidden in all others.



The <b>Frequent</b> and <b>Recent</b> categories are likely to contain a degree of overlap and therefore you should not add both categories to a single Jump List. Which of the two is best for your application depends on its nature. An application that generates files, such as Microsoft Word or Microsoft Paint, should use the <b>Recent</b> category as users are most likely to want to return to files that they have recently worked on. An application that is used more for browsing or playback of data created elsewhere should use the <b>Frequent</b> category because the user is more likely to access a greater number of items, many of them only once. In other words, if your application is most likely to access a large number of items only a few times each, which contributes noise to the smaller set of items users want to access many times, then <b>Frequent</b> is the best choice. If your application is more likely to access a smaller number of newer items most of the time, then you should choose <b>Recent</b>.

Categories in a custom Jump List, including the known <b>Recent</b> or <b>Frequent</b> category, are shown in the order that they are added, with the most recently added categories at the bottom of the list.

Any number of destinations added over the value pointed to by the <i>pcMinItems</i> parameter in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> are not shown.

Empty categories are not shown.

The contents of the <b>Frequent</b> and <b>Recent</b> categories are calculated for each application that uses <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> directly. In some cases of user action, such as opening a file through Windows Explorer or using the common file dialog box to open, save, or create a file, the Shell calls <b>SHAddToRecentDocs</b> on behalf of an application and those calls are also taken into account in the usage statistics. The Shell also calls <b>SHAddToRecentDocs</b> on behalf of the application when a destination is launched from its Jump List. However, it is good practice for the application to explicitly call <b>SHAddToRecentDocs</b> itself even if it is expected that the Shell will make the call. This guarantees that the usage is recorded, and the algorithms for tracking recent or frequent usage will correct for any duplicate calls.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks">ICustomDestinationList::AddUserTasks</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">ICustomDestinationList::AppendCategory</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
