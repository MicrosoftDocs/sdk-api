---
UID: NS:mmc._RESULT_VIEW_TYPE_INFO
title: "_RESULT_VIEW_TYPE_INFO"
author: windows-sdk-content
description: The RESULT_VIEW_TYPE_INFO structure is introduced in MMC 2.0.
old-location: mmc\result_view_type_info.htm
old-project: MMC
ms.assetid: 50357902-6999-4d65-8e12-81277b66d5ee
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PRESULT_VIEW_TYPE_INFO, MMC_VIEW_TYPE_HTML, MMC_VIEW_TYPE_LIST, MMC_VIEW_TYPE_OCX, RESULT_VIEW_TYPE_INFO, RESULT_VIEW_TYPE_INFO structure [MMC], RVTI_LIST_OPTIONS_ALLOWPASTE, RVTI_LIST_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST, RVTI_LIST_OPTIONS_FILTERED, RVTI_LIST_OPTIONS_LEXICAL_SORT, RVTI_LIST_OPTIONS_MULTISELECT, RVTI_LIST_OPTIONS_NONE, RVTI_LIST_OPTIONS_OWNERDATALIST, RVTI_LIST_OPTIONS_USEFONTLINKING, RVTI_OCX_OPTIONS_CACHE_OCX, RVTI_OCX_OPTIONS_NOLISTVIEW, RVTI_OCX_OPTIONS_NONE, _RESULT_VIEW_TYPE_INFO, _slate_result_view_type_info, mmc.result_view_type_info, mmc/RESULT_VIEW_TYPE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RESULT_VIEW_TYPE_INFO, *PRESULT_VIEW_TYPE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - RESULT_VIEW_TYPE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _RESULT_VIEW_TYPE_INFO structure


## -description


The <b>RESULT_VIEW_TYPE_INFO</b> structure is introduced in MMC 2.0.

The <b>RESULT_VIEW_TYPE_INFO</b> structure is used in calls to 
<a href="https://msdn.microsoft.com/687ddb0a-6e10-4553-9885-fd85bf8dd6ff">IComponent2::GetResultViewType2</a> and 
<a href="https://msdn.microsoft.com/fe9a71c7-eaa6-4479-8337-0746a784a57f">IComponent2::RestoreResultView</a>. A snap-in uses these two methods to include a result view in the navigational order maintained by MMC's 
<b>Back</b>/<b>Forward</b> buttons.


## -struct-fields




### -field pstrPersistableViewDescription

Snap-in-provided identifier for this view type. When implementing <a href="https://msdn.microsoft.com/687ddb0a-6e10-4553-9885-fd85bf8dd6ff">IComponent2::GetResultViewType2</a>, this member must contain a valid view description string; otherwise, MMC will not initialize your snap-in. Additionally, this value must be created by means of <a href="https://msdn.microsoft.com/en-us/library/ms692727(v=VS.85).aspx">CoTaskMemAlloc</a>. It will be freed by MMC, not the snap-in.


### -field eViewType


<a href="https://msdn.microsoft.com/fffb7376-bf1d-44ce-ad52-d4c45d013af7">MMC_VIEW_TYPE</a> enumeration value specifying the view type. This member is the structure's union discriminator and determines which members of the union are valid. This member is one of the following values.



#### MMC_VIEW_TYPE_LIST

This view is a list view.



#### MMC_VIEW_TYPE_HTML

This view is an HTML view.



#### MMC_VIEW_TYPE_OCX

This view is an OCX (ActiveX control) view.


### -field dwMiscOptions

A value that specifies whether the view contains list views. If this value is <b>RVTI_MISC_OPTIONS_NOLISTVIEWS</b>, no list views are contained in the view (the console refrains from presenting standard list view choices on the <b>View</b> menu). Otherwise, this value is zero.


### -field dwListOptions

A value that specifies the list view options. Applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_LIST</b>. This value can be one or more of the following values.



#### RVTI_LIST_OPTIONS_NONE

No view options selected. This is the default view option.



#### RVTI_LIST_OPTIONS_OWNERDATALIST

A value that specifies that the result pane list view should be a virtual list.



#### RVTI_LIST_OPTIONS_MULTISELECT

Allows multiple item selections in the result pane view.



#### RVTI_LIST_OPTIONS_FILTERED

Notifies MMC that the snap-in supports filtered views. See <a href="https://msdn.microsoft.com/4be29e44-7e64-4c2c-820b-26c6cfea0661">Adding Filtered Views</a>.



#### RVTI_LIST_OPTIONS_USEFONTLINKING

Uses font linking on result items (for multilingual support). Font linking is a feature installed on systems with Microsoft Internet Explorer version 4.0 or later. Given a Unicode string, the font linking feature determines the best font for that displays that string. For example, to populate a list view with server names in both Japanese and Russian, you would set the font linking view options, and MMC would determine an appropriate font. In the default setting, font linking is not enabled because it can cause a short delay while MMC searches for the appropriate font.



#### RVTI_LIST_OPTIONS_EXCLUDE_SCOPE_ITEMS_FROM_LIST

Causes MMC to hide scope items in the view; this applies to standard list views. Scope items are hidden in virtual list views.



#### RVTI_LIST_OPTIONS_LEXICAL_SORT

Causes MMC to lexically sort all scope items (including extensions) first, followed by all result items; this applies to standard list views. The <a href="https://msdn.microsoft.com/7a68713c-2de5-4944-a617-0b2d46c23eea">IResultDataCompare</a> and <a href="https://msdn.microsoft.com/e4b305e4-4649-42f4-86f4-3c12e5aa5337">IResultDataCompareEx</a> interfaces are ignored when this value is set.



#### RVTI_LIST_OPTIONS_ALLOWPASTE

Informs MMC that the result pane item is a drop target (see <a href="https://msdn.microsoft.com/a48823af-2de6-465b-913c-7cdcdbd04040">Using Drag and Drop to Result Pane Items</a>).


### -field dwHTMLOptions

Applies only when <b>eViewType</b> is <b>MMC_VIEW_TYPE_HTML</b>. This value is reserved for future use and must be zero.


### -field pstrURL

The URL for the HTML view. This parameter applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_HTML</b>.


### -field dwOCXOptions

Applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_OCX</b>. This value can be one or more of the following values.

<div class="alert"><b>Note</b>  Once the OCX caching option has been set (either by using or not using the <b>RVTI_OCX_OPTIONS_CACHE_OCX</b> flag), the option choice for this instance of the snap-in must not be changed.</div>
<div> </div>


#### RVTI_OCX_OPTIONS_NONE

No options are specified for the OCX view.



#### RVTI_OCX_OPTIONS_NOLISTVIEW

There is no list view in the OCX view.



#### RVTI_OCX_OPTIONS_CACHE_OCX

MMC will cache the OCX. If this value is specified, then the snap-in should maintain the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer for the OCX, so that if MMC calls <a href="https://msdn.microsoft.com/687ddb0a-6e10-4553-9885-fd85bf8dd6ff">IComponent2::GetResultViewType2</a> again, the snap-in returns the <b>IUnknown</b> pointer. MMC then identifies the cached OCX and reuses it. 
Be aware that OCXs are cached for each <a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> object, so the snap-in should create a different OCX for each <b>IComponent</b> object even if<b> RVTI_OCX_OPTIONS_CACHE_OCX</b> is set.


### -field pUnkControl

The <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer for the OCX. This parameter applies only when the <b>eViewType</b> member is <b>MMC_VIEW_TYPE_OCX</b>. When a snap-in implements <a href="https://msdn.microsoft.com/b9e67a37-c09d-46f3-896f-e75122256812">IComponent2</a> and has an OCX in the result pane, the snap-in must create the OCX during the call to <a href="https://msdn.microsoft.com/687ddb0a-6e10-4553-9885-fd85bf8dd6ff">IComponent2::GetResultViewType2</a> and return the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer (through <b>pUnkControl</b>) to MMC. The snap-in must also initialize the OCX. MMC will not send a <a href="https://msdn.microsoft.com/79256d4a-a936-419e-a953-80d743d05290">MMCN_INITOCX</a> notification to the snap-in.


## -see-also




<a href="https://msdn.microsoft.com/687ddb0a-6e10-4553-9885-fd85bf8dd6ff">IComponent2::GetResultViewType2</a>



<a href="https://msdn.microsoft.com/fe9a71c7-eaa6-4479-8337-0746a784a57f">IComponent2::RestoreResultView</a>



<a href="https://msdn.microsoft.com/dee09c50-76f1-4186-846c-1cde3d05fd03">Restoring Result Views</a>



<a href="https://msdn.microsoft.com/a48823af-2de6-465b-913c-7cdcdbd04040">Using Drag and Drop to Result Pane Items</a>
 

 

