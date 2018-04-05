---
UID: NF:icm.CreateMultiProfileTransform
title: CreateMultiProfileTransform function
author: windows-driver-content
description: The CreateMultiProfileTransform function accepts an array of profiles or a single device link profile and creates a color transform that applications can use to perform color mapping.
old-location: wcs\createmultiprofiletransform.htm
old-project: WCS
ms.assetid: bf344e44-1379-4ba5-8215-57001c53bbd5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CreateMultiProfileTransform, CreateMultiProfileTransform function [Windows Color System], INTENT_ABSOLUTE_COLORIMETRIC, INTENT_PERCEPTUAL, INTENT_RELATIVE_COLORIMETRIC, INTENT_SATURATION, _color_CreateMultiProfileTransform, icm/CreateMultiProfileTransform, wcs.createmultiprofiletransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mscms.dll
api_name:
-	CreateMultiProfileTransform
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# CreateMultiProfileTransform function


## -description


The <b>CreateMultiProfileTransform</b> function accepts an array of profiles or a single <a href="d.htm">device link profile</a> and creates a color transform that applications can use to perform color mapping.


## -parameters




### -param pahProfiles

Pointer to an array of handles to the profiles to be used. The function determines whether the HPROFILEs contain International Color Consortium (ICC) or Windows Color System (WCS) profile information and processes them appropriately. When valid WCS profiles are returned by <a href="https://msdn.microsoft.com/5f738012-690f-4ff9-bc40-4ccbd47169c6">OpenColorProfile</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff563736">WcsOpenColorProfile</a>, these profile handles contain the combination of DMP, CAMP, and GMMP profiles.


### -param nProfiles

Specifies the number of profiles in the array. The maximum is 10.


### -param padwIntent

Pointer to an array of intents to use. Each intent is one of the following values:

<a id="INTENT_PERCEPTUAL"></a>
<a id="intent_perceptual"></a>


#### INTENT_PERCEPTUAL

<a id="INTENT_SATURATION"></a>
<a id="intent_saturation"></a>


#### INTENT_SATURATION

<a id="INTENT_RELATIVE_COLORIMETRIC"></a>
<a id="intent_relative_colorimetric"></a>


#### INTENT_RELATIVE_COLORIMETRIC

<a id="INTENT_ABSOLUTE_COLORIMETRIC"></a>
<a id="intent_absolute_colorimetric"></a>


#### INTENT_ABSOLUTE_COLORIMETRIC

GMMPs are a generalization of intents. There are two possible sources of intents: the "destination" profile and the intent list parameter to <b>CreateMultiProfileTransform</b>. The term "destination" is not used since all but two of the profiles in the profile list parameter will serve as first destination and then source.

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param nIntents

Specifies the number of elements in the intents array: can either be 1 or the same value as <i>nProfiles</i>. For profile arrays that contain any WCS profiles, the first rendering intent is ignored and only <i>nProfiles</i> -1 elements are used for these profile arrays. The maximum number of <i>nIntents</i> is 10.


### -param dwFlags

Specifies flags used to control creation of the transform. See Remarks.


### -param indexPreferredCMM

Specifies the one-based index of the color profile that indicates what color management module (CMM) to use. The application developer may allow Windows to choose the CMM by setting this parameter to INDEX_DONT_CARE. See <a href="https://msdn.microsoft.com/df119e1a-b6f5-40a3-8852-8a57b21483d0">Using Color Management Modules (CMM)</a> Third party CMMs are only available for ICC workflows. Profile arrays containing WCS profiles will ignore this flag. It is also ignored when only ICC profiles are used and when the WCS_ALWAYS flag is used.


## -returns



If this function succeeds, the return value is a handle to the color transform.

If this function fails, the return value is <b>NULL</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If a device link profile is being used, the function will fail if <i>nProfiles</i> is not set to 1.

The array of intents specifies how profiles should be combined. The <i>n</i>th intent is used for combining the <i>n</i>th profile in the array. If only one intent is specified, it is used for the first profile, and all other profiles are combined using <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Match intent</a>.

The values in <i>dwFlags</i> are intended as hints only. The color management module must determine the best way to use them.

<b>Windows Vista</b>: Three new flags have been added that can be used with <i>dwFlags</i>:

<table>
<tr>
<td><b>PRESERVEBLACK</b></td>
<td>If this bit is set, the transform engine inserts the appropriate black generation GMMP as the last GMMP in the transform sequence. This flag only works in a pure WCS transform.</td>
</tr>
<tr>
<td><b>SEQUENTIAL_TRANSFORM</b></td>
<td>If this bit is set, each step in the WCS processing pipeline is performed for every pixel in the image and no optimized color transform is built. This flag only works in a pure WCS transform.<b>Restrictions</b>: A transform created with the SEQUENTIAL_TRANSFORM flag set may only be used in the thread on which it was created and only for one color translation call at a time. COM must be initialized prior to creating the sequential transform and must remain initialized for the lifetime of the transform object.

</td>
</tr>
<tr>
<td><b>WCS_ALWAYS</b></td>
<td>If this bit is set, even all-ICC transforms will use the WCS code path.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  <p class="note">SEQUENTIAL_TRANSFORM was inadvertently omitted from the icm.h header in the Windows Vista SDK. If you wish to use the SEQUENTIAL_TRANSFORM flag, define it in your application as follows:

<p class="note">#define SEQUENTIAL_TRANSFORM 0x80800000

</div>
<div> </div>
For details, see <a href="https://msdn.microsoft.com/f3942929-272c-4f08-98ac-a4d14d2f6ac4">CMM Transform Creation Flags</a>. All of the flags mentioned there are supported for all types of transforms, except for FAST_TRANSLATE and USE_RELATIVE_COLORIMETRIC, which only work in a pure ICC-to-ICC transform.

The <b>CreateMultiProfileTransform</b> function is used outside of a device context. Colors may shift when transforming from a color profile to the same color profile. This is due to precision errors. Therefore, a color transform should not be performed under these circumstances.

We recommend that there be only one GMMP between a source and destination DMP. Gamut boundary descriptions (GBDs) are created from the DMP/CAMP combinations. The subsequent GMMPs use the GDBs prior to them in the processing chain until there exists a DMP/CAMP GBD next in the sequence to be used. For example, assume a sequence DMP1, CAMP1, GMMP1, GMMP2, GMMP3, DMP2, CAMP2, GMMP4, GMMP5, CAMP3, DMP3. Then GMMP1, GMMP2 use GBD1 as their source and destination. Then GMMP3 uses GBD1 as source and GBD2 as destination. Then GMMP4 uses GBD2 as source and destination. Finally GMMP5 uses GBD2 as source and GBD3 as destination. This assumes no GMMP is identical to one next to it.

For WCS profiles, we recommend that the rendering intents be set to DWORD_MAX in order to use the GMMP within the WCS profile handle. This is because the array of rendering intents takes precedence over the rendering intents or gamut mapping models specified or contained in the profiles specified by the HPROFILEs. The array of rendering intents references the default GMMP for those rendering intents. Ideally, only one gamut mapping is performed between a source and destination device by setting one or the other GMMP to <b>NULL</b> when creating the HPROFILE with WCS profile information. Any legacy application that uses a WCS DMP will invoke a sequence of GMMPs. GDBs are chosen based on DMPs and CAMPs. For intermediate GMMP gamut boundaries, the source and destination GBDs are used.

In summary, if <i>nIntents</i> == 1, then the first GMM is set based on the GMMP that is set as default* for the <i>padwIntent</i> value, unless that value is DWORD_MAX, in which case the embedded GMM information from the second profile is used (The embedded GMM information is either a GMMP or, in the case of an ICC profile, the baseline GMM corresponding to** the intent from the profile header). The remainder of the GMMs are set based on the GMMP that is set as default* for RelativeColorimetric.

If <i>nIntents</i> = <i>nProfiles</i> -1, then each GMM is set based on the GMMP that is set as default* for the value in the <i>padwIntent</i> array at the corresponding index, except where <i>padwIntent</i> values are DWORD_MAX. For values in the <i>padwIntent</i> array that are DWORD_MAX, the GMMs at corresponding positions are set based on the embedded GMM information from the second of the two profiles whose gamuts are mapped by the GMM. (Again, the embedded GMM information is either a GMMP or, in the case of an ICC profile, the baseline GMM corresponding to** the intent from the profile header).

If <i>nIntents</i> = <i>nProfiles</i>, then first intent is ignored and funtion behaves as it does in the case when <i>nIntents</i> = <i>nProfiles</i> -1.

Any other combination of <i>padwIntents</i> and <i>nIntents</i> will return an error.

* "set as default" means that the default GMMP is queried using <b>WcsGetDefaultColorProfile</b> with its <i>profileManagementScope</i> parameter set to WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER. This may return either current-user or system-wide defaults as described in the documentation for <b>WcsGetDefaultColorProfile</b>.

** "GMM corresponding to" does not mean "GMM from the GMMP set as default for". Instead it means "a constant association between ICC profile intents and baseline GMM algorithms."

WCS transform support for ICC ColorSpace profiles is limited to RGB colorspace profiles. The following ICC profile types cannot be used in a CITE-processed transform, either a mixed WCS/ICC transform or an all-ICC transform with <b>WCS_ALWAYS</b> set:

<ul>
<li>Non-RGB ColorSpace profiles</li>
<li>NamedColor profiles</li>
<li>n-channel profiles (where n &gt; 8)</li>
<li>DeviceLink profiles</li>
<li>Abstract profiles</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/2efd98d8-851f-4a6c-b91b-2430895a7a53">DeleteColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="color.htm">The COLOR Structure</a>
 

 

