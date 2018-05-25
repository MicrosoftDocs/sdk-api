---
UID: TP:tablet
ms.assetid: 8f8b94e8-8687-3dab-9a34-5a6464070552
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Tablet PC



Overview of the Tablet PC technology.

To develop Tablet PC, you need these headers:

 * [inked.h](..\inked\index.md)
 * [micaut.h](..\micaut\index.md)
 * [msinkaut.h](..\msinkaut\index.md)
 * [msinkaut15.h](..\msinkaut15\index.md)
 * [peninputpanel.h](..\peninputpanel\index.md)
 * [recapis.h](..\recapis\index.md)
 * [rectypes.h](..\rectypes\index.md)
 * [rtscom.h](..\rtscom\index.md)
 * [tabflicks.h](..\tabflicks\index.md)
 * [tpcshrd.h](..\tpcshrd\index.md)

For the programming guide, see [Tablet PC](/windows/desktop/tablet).

## Functions

| Title   | Description   |
| ---- |:---- |
| [AddStroke function](..\recapis\nf-recapis-addstroke.md) | Adds an ink stroke to the RecognizerContext. |
| [AddWordsToWordList function](..\recapis\nf-recapis-addwordstowordlist.md) | Adds one or more words to the word list. |
| [AdviseInkChange function](..\recapis\nf-recapis-adviseinkchange.md) | Stops the recognizer from processing ink because a stroke has been added or deleted. |
| [CloneContext function](..\recapis\nf-recapis-clonecontext.md) | Creates a recognizer context that contains the same settings as the original. The new recognizer context does not include the ink or recognition results of the original. |
| [CreateContext function](..\recapis\nf-recapis-createcontext.md) | Creates a recognizer context. |
| [CreateRecognizer function](..\recapis\nf-recapis-createrecognizer.md) | Creates a recognizer. |
| [DestroyAlternate function](..\recapis\nf-recapis-destroyalternate.md) | This function is obsolete and need not be implemented by custom application recognizers. |
| [DestroyContext function](..\recapis\nf-recapis-destroycontext.md) | Destroys a recognizer context. |
| [DestroyRecognizer function](..\recapis\nf-recapis-destroyrecognizer.md) | Destroys a recognizer. |
| [DestroyWordList function](..\recapis\nf-recapis-destroywordlist.md) | Destroys the current word list. |
| [EndInkInput function](..\recapis\nf-recapis-endinkinput.md) | Indicates that no more ink will be added to the context.You cannot add strokes to the context after calling this function. |
| [GetAllRecognizers function](..\recapis\nf-recapis-getallrecognizers.md) | Gets all recognizers. |
| [GetBestResultString function](..\recapis\nf-recapis-getbestresultstring.md) | Retrieves the best result string. |
| [GetContextPreferenceFlags function](..\recapis\nf-recapis-getcontextpreferenceflags.md) | Gets the context preference flags. |
| [GetContextPropertyList function](..\recapis\nf-recapis-getcontextpropertylist.md) | Retrieves a list of properties the recognizer supports. |
| [GetContextPropertyValue function](..\recapis\nf-recapis-getcontextpropertyvalue.md) | Returns a specified property value from the recognizer context. |
| [GetEnabledUnicodeRanges function](..\recapis\nf-recapis-getenabledunicoderanges.md) | Retrieves a list of Unicode point ranges enabled on the context. If you do not call the SetEnabledUnicodeRanges function to specify the enabled ranges, this function returns the recognizer's default Unicode point ranges. |
| [GetGuide function](..\recapis\nf-recapis-getguide.md) | Retrieves the guide used for boxed, lined, or freeform input. |
| [GetLatticePtr function](..\recapis\nf-recapis-getlatticeptr.md) | Retrieves a pointer to the lattice for the current results. |
| [GetLeftSeparator function](..\recapis\nf-recapis-getleftseparator.md) | Gets the left separator for the recognizer context. |
| [GetPreferredPacketDescription function](..\recapis\nf-recapis-getpreferredpacketdescription.md) | Retrieves a packet description that contains the packet properties the recognizer uses. |
| [GetRecoAttributes function](..\recapis\nf-recapis-getrecoattributes.md) | Retrieves the attributes of the recognizer. |
| [GetResultPropertyList function](..\recapis\nf-recapis-getresultpropertylist.md) | Retrieves a list of properties the recognizer can return for a result range. |
| [GetRightSeparator function](..\recapis\nf-recapis-getrightseparator.md) | Gets the right separator for the recognizer context. |
| [GetUnicodeRanges function](..\recapis\nf-recapis-getunicoderanges.md) | Returns the ranges of Unicode points that the recognizer supports. |
| [IsStringSupported function](..\recapis\nf-recapis-isstringsupported.md) | Returns a value that indicates whether a word, date, time, number, or other text that is passed in is contained in the dictionary.The results of this test depend on the factoid setting. |
| [LoadCachedAttributes function](..\recapis\nf-recapis-loadcachedattributes.md) | Loads the cached attributes of a recognizer. |
| [MakeWordList function](..\recapis\nf-recapis-makewordlist.md) | Creates a word list. |
| [Process function](..\recapis\nf-recapis-process.md) | Performs ink recognition synchronously. |
| [ResetContext function](..\recapis\nf-recapis-resetcontext.md) | Deletes the current ink and recognition results from the context.The current settings of the recognizer context are preserved. |
| [SetCACMode function](..\recapis\nf-recapis-setcacmode.md) | Specifies character Autocomplete mode for character or word recognition.You cannot turn off character Autocomplete after it is set. |
| [SetContextPropertyValue function](..\recapis\nf-recapis-setcontextpropertyvalue.md) | Adds a property to the recognizer context.If a property already exists, its value is modified. |
| [SetEnabledUnicodeRanges function](..\recapis\nf-recapis-setenabledunicoderanges.md) | Enables one or more Unicode point ranges on the context. |
| [SetFactoid function](..\recapis\nf-recapis-setfactoid.md) | Specifies the factoid a recognizer uses to constrain its search for the result.You specify a factoid if an input field is of a known type, such as if the input field contains a date. |
| [SetFlags function](..\recapis\nf-recapis-setflags.md) | Specifies how the recognizer interprets the ink and determines the result string.Call this function before processing the ink for the first time. Therefore, call the SetFlags function before calling the Process function. |
| [SetGuide function](..\recapis\nf-recapis-setguide.md) | Sets the recognition guide to use for boxed or lined input. You must call this function before you add strokes to the context. |
| [SetTextContext function](..\recapis\nf-recapis-settextcontext.md) | Provides the text strings that come before and after the text contained in the recognizer context.You call this function before processing the ink for the first time. Therefore, call the SetTextContext function before calling the Process function. |
| [SetWordList function](..\recapis\nf-recapis-setwordlist.md) | Sets the word list for the current recognizer context to recognize. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [FLICK_DATA structure](..\tabflicks\ns-tabflicks-flick_data.md) | Contains information about a pen flick. |
| [FLICK_POINT structure](..\tabflicks\ns-tabflicks-flick_point.md) | Provides information about a pen flick. |
| [IEC_GESTUREINFO structure](..\inked\ns-inked-iec_gestureinfo.md) | Contains information about a specific gesture. |
| [IEC_RECOGNITIONRESULTINFO structure](..\inked\ns-inked-iec_recognitionresultinfo.md) | Contains information about an IInkRecognitionResult Interface object. |
| [IEC_STROKEINFO structure](..\inked\ns-inked-iec_strokeinfo.md) | Contains information about a Stroke event. |
| [StylusInfo structure](..\rtscom\ns-rtscom-stylusinfo.md) | Provides information about the stylus. |
| [_InkRecoGuide structure](..\msinkaut\ns-msinkaut-_inkrecoguide.md) | Deprecated. Represents information about the recognition guide. Use the WritingBox Property, DrawnBox Property, Rows Property, Columns Property, and Midline Property [InkRecognizerGuide Class] properties instead. |
| [_PACKET_DESCRIPTION structure](..\tpcshrd\ns-tpcshrd-_packet_description.md) | Describes the content of the packet for a particular tablet recognizer context.Do not use this structure to access the data contained in a packet. This structure describes the content of the packet. |
| [_PACKET_PROPERTY structure](..\tpcshrd\ns-tpcshrd-_packet_property.md) | Describes a packet property that is reported by the tablet driver. |
| [_PROPERTY_METRICS structure](..\tpcshrd\ns-tpcshrd-_property_metrics.md) | Defines the range and resolution of a packet property. |
| [tagCHARACTER_RANGE structure](..\rectypes\ns-rectypes-tagcharacter_range.md) | Specifies a range of Unicode points (characters). |
| [tagINKMETRIC structure](..\msinkaut\ns-msinkaut-taginkmetric.md) | Specifies display properties for a text ink object (tInk). |
| [tagLATTICE_METRICS structure](..\rectypes\ns-rectypes-taglattice_metrics.md) | Describes the baseline and the midline height. |
| [tagLINE_SEGMENT structure](..\rectypes\ns-rectypes-tagline_segment.md) | Describes the start and end points of a line recognition segment, such as the baseline or midline. |
| [tagRECO_ATTRS structure](..\rectypes\ns-rectypes-tagreco_attrs.md) | Retrieves the attributes of a recognizer or specifies which attributes to use when you search for an installed recognizer. |
| [tagRECO_GUIDE structure](..\rectypes\ns-rectypes-tagreco_guide.md) | Defines the boundaries of the ink to the recognizer. |
| [tagRECO_LATTICE structure](..\rectypes\ns-rectypes-tagreco_lattice.md) | Serves as the entry point into a lattice. |
| [tagRECO_LATTICE_COLUMN structure](..\rectypes\ns-rectypes-tagreco_lattice_column.md) | Represents a column in the lattice. |
| [tagRECO_LATTICE_ELEMENT structure](..\rectypes\ns-rectypes-tagreco_lattice_element.md) | Corresponds to one word or one East Asian character, typically; however, an element may also correspond to a gesture, a shape, or some other code. |
| [tagRECO_LATTICE_PROPERTIES structure](..\rectypes\ns-rectypes-tagreco_lattice_properties.md) | Contains an array of pointers to property structures. |
| [tagRECO_LATTICE_PROPERTY structure](..\rectypes\ns-rectypes-tagreco_lattice_property.md) | Contains a property used in the lattice. |
| [tagRECO_RANGE structure](..\rectypes\ns-rectypes-tagreco_range.md) | The structure is obsolete. |
| [tagSTROKE_RANGE structure](..\tpcshrd\ns-tpcshrd-tagstroke_range.md) | Specifies a range of strokes in the InkDisp object. |
| [tagSYSTEM_EVENT_DATA structure](..\tpcshrd\ns-tpcshrd-tagsystem_event_data.md) | Contains information about a tablet system event. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [AppearanceConstants enumeration](..\inked\ne-inked-appearanceconstants.md) | Specifies how an InkEdit control appears on the screen. |
| [BorderStyleConstants enumeration](..\inked\ne-inked-borderstyleconstants.md) | Specifies how the borders of an InkEdit control appear on the screen. |
| [DISPID_InkRecognizerGuide enumeration](..\msinkaut\ne-msinkaut-dispid_inkrecognizerguide.md) | Deprecated. Represents information about the recognition guide. Use the WritingBox Property, DrawnBox Property, Rows Property, Columns Property, and Midline Property [InkRecognizerGuide Class] properties instead. |
| [FLICKACTION_COMMANDCODE enumeration](..\tabflicks\ne-tabflicks-flickaction_commandcode.md) | Defines the possible flick actions that can be assigned to a pen flick. |
| [FLICKDIRECTION enumeration](..\tabflicks\ne-tabflicks-flickdirection.md) | Defines the directions in which a pen flick has occurred. |
| [FLICKMODE enumeration](..\tabflicks\ne-tabflicks-flickmode.md) | Describes where Flick gestures are enabled. |
| [InkApplicationGesture enumeration](..\msinkaut\ne-msinkaut-inkapplicationgesture.md) | Defines values that set the interest in a set of application-specific gesture. |
| [InkBoundingBoxMode enumeration](..\msinkaut\ne-msinkaut-inkboundingboxmode.md) | Specifies which characteristics of a stroke, such as drawing attributes, are used to calculate the bounding box of the ink.The bounding box is the smallest rectangle that includes all points in the InkDisp object. |
| [InkClipboardFormats enumeration](..\msinkaut\ne-msinkaut-inkclipboardformats.md) | Specifies the format of ink that is stored on the Clipboard. |
| [InkClipboardModes enumeration](..\msinkaut\ne-msinkaut-inkclipboardmodes.md) | Specifies the copy options of the Clipboard. |
| [InkCollectionMode enumeration](..\msinkaut\ne-msinkaut-inkcollectionmode.md) | Defines values that determine whether ink, gestures, or ink and gestures are recognized as the user writes. |
| [InkCollectorEventInterest enumeration](..\msinkaut\ne-msinkaut-inkcollectoreventinterest.md) | Defines values that are used to specify whether an event occurred on an ink collector and, if so, which event fired. |
| [InkCursorButtonState enumeration](..\msinkaut\ne-msinkaut-inkcursorbuttonstate.md) | Defines values that specify the state of a cursor button. |
| [InkDisplayMode enumeration](..\inked\ne-inked-inkdisplaymode.md) | Specifies how a selection appears on the control. |
| [InkEditStatus enumeration](..\inked\ne-inked-inkeditstatus.md) | Specifies whether the InkEdit control is idle, collecting ink, or recognizing ink. |
| [InkExtractFlags enumeration](..\msinkaut\ne-msinkaut-inkextractflags.md) | Determines how a stroke is removed from an InkDisp object. |
| [InkInsertMode enumeration](..\inked\ne-inked-inkinsertmode.md) | Specifies how ink is inserted onto the InkEdit control. |
| [InkMode enumeration](..\inked\ne-inked-inkmode.md) | Specifies the collection mode for drawn ink-whether ink collection is disabled, ink is collected, or ink and gestures are collected. |
| [InkMouseButton enumeration](..\msinkaut\ne-msinkaut-inkmousebutton.md) | Specifies which mouse button was pressed. |
| [InkMousePointer enumeration](..\msinkaut\ne-msinkaut-inkmousepointer.md) | Specifies the type of mouse pointer to appear. |
| [InkOverlayAttachMode enumeration](..\msinkaut\ne-msinkaut-inkoverlayattachmode.md) | Specifies where to attach the new InkOverlay object, behind or in front of the active layer. |
| [InkOverlayEditingMode enumeration](..\msinkaut\ne-msinkaut-inkoverlayeditingmode.md) | Specifies the behavior mode of the InkOverlay object and the InkPicture control. |
| [InkOverlayEraserMode enumeration](..\msinkaut\ne-msinkaut-inkoverlayerasermode.md) | Specifies the way in which ink is erased from the InkOverlay object and the InkPicture control.This mode is used when the InkOverlayEditingMode is set to Delete. |
| [InkPenTip enumeration](..\msinkaut\ne-msinkaut-inkpentip.md) | Specifies the pen-tip shape. |
| [InkPersistenceCompressionMode enumeration](..\msinkaut\ne-msinkaut-inkpersistencecompressionmode.md) | Defines values for the compression modes that are used to save the InkDisp object to a serialized format. |
| [InkPersistenceFormat enumeration](..\msinkaut\ne-msinkaut-inkpersistenceformat.md) | Specifies how ink is persisted. |
| [InkPictureSizeMode enumeration](..\msinkaut\ne-msinkaut-inkpicturesizemode.md) | Specifies how the picture behaves inside the InkPicture control. |
| [InkRasterOperation enumeration](..\msinkaut\ne-msinkaut-inkrasteroperation.md) | Defines values for performing raster operations on drawn ink. |
| [InkRecognitionAlternatesSelection enumeration](..\msinkaut\ne-msinkaut-inkrecognitionalternatesselection.md) | Not implemented. |
| [InkRecognitionConfidence enumeration](..\msinkaut\ne-msinkaut-inkrecognitionconfidence.md) | Indicates the level of confidence that the recognizer has in the recognition result. |
| [InkRecognitionModes enumeration](..\msinkaut\ne-msinkaut-inkrecognitionmodes.md) | Specifies how the recognizer interprets the ink and determines the result string. |
| [InkRecognitionStatus enumeration](..\msinkaut\ne-msinkaut-inkrecognitionstatus.md) | Specifies whether an error occurred during recognition and, if so, which error occurred. |
| [InkRecognizerCapabilities enumeration](..\msinkaut\ne-msinkaut-inkrecognizercapabilities.md) | Specifies the attributes of a recognizer. You also use this enumeration to determine which attributes to use when you search for an installed recognizer. |
| [InkRecognizerCharacterAutoCompletionMode enumeration](..\msinkaut\ne-msinkaut-inkrecognizercharacterautocompletionmode.md) | Specifies types of character input modes. |
| [InkShiftKeyModifierFlags enumeration](..\msinkaut\ne-msinkaut-inkshiftkeymodifierflags.md) | Specifies which modifier key was pressed. |
| [InkSystemGesture enumeration](..\msinkaut\ne-msinkaut-inksystemgesture.md) | Specifies the interest in a set of operating system-specific gestures. |
| [ItemSelectionConstants enumeration](..\msinkaut\ne-msinkaut-itemselectionconstants.md) | Specifies whether the first element or all elements within a group of points or packet values are used. |
| [KEYMODIFIER enumeration](..\tabflicks\ne-tabflicks-keymodifier.md) | Determines which, if any, modifier keys were pressed when the flick gesture occurred. |
| [MouseButton enumeration](..\inked\ne-inked-mousebutton.md) | Specifies which mouse button was pressed. |
| [RealTimeStylusDataInterest enumeration](..\rtscom\ne-rtscom-realtimestylusdatainterest.md) | Defines the values used by plug-ins to specify which event notifications the plug-ins receive. |
| [RealTimeStylusLockType enumeration](..\rtscom\ne-rtscom-realtimestyluslocktype.md) | Specifies the locks within the RealTimeStylus Class object that protect the RealTimeStylus Class object's members and properties from modification. |
| [SCROLLDIRECTION enumeration](..\tabflicks\ne-tabflicks-scrolldirection.md) | Defines the direction of the scrolling command for a pen flick. |
| [ScrollBarsConstants enumeration](..\inked\ne-inked-scrollbarsconstants.md) | Specifies how the scroll bars of an InkEdit control appear on the screen. |
| [SelAlignmentConstants enumeration](..\inked\ne-inked-selalignmentconstants.md) | Specifies the alignment of the paragraph relative to the margins of the InkEdit control. |
| [SelectionHitResult enumeration](..\msinkaut\ne-msinkaut-selectionhitresult.md) | Specifies which part of a selection, if any, was hit during a hit test. |
| [StylusQueue enumeration](..\rtscom\ne-rtscom-stylusqueue.md) | Specifies the queue to which stylus data is added. |
| [TabletHardwareCapabilities enumeration](..\msinkaut\ne-msinkaut-tablethardwarecapabilities.md) | Specifies the hardware capabilities of the Tablet PC. |
| [TabletPropertyMetricUnit enumeration](..\msinkaut\ne-msinkaut-tabletpropertymetricunit.md) | Indicates the unit of measurement of a property. |
| [_PROPERTY_UNITS enumeration](..\tpcshrd\ne-tpcshrd-_property_units.md) | Defines constant values for the unit of measurement of a property. |
| [__MIDL___MIDL_itf_micaut_0000_0000_0001 enumeration](..\micaut\ne-micaut-__midl___midl_itf_micaut_0000_0000_0001.md) | Specifies the user interface (UI) elements of a math input control (MIC). |
| [__MIDL___MIDL_itf_micaut_0000_0000_0002 enumeration](..\micaut\ne-micaut-__midl___midl_itf_micaut_0000_0000_0002.md) | Specifies the button states of a math input control (MIC). |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0001 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0001.md) | Specifies the interaction modes that can be chosen by the user for the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0002 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0002.md) | Specifies the In-Place state values of the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0003 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0003.md) | Specifies the values that represent the default input areas of the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0004 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0004.md) | Specifies the correction modes of the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0005 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0005.md) | Specifies the direction, relative to Input Panel, that the post insertion correction comb displays. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0006 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0006.md) | Specifies the preferred direction of the In-Place Input Panel relative to the text entry field. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0007 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0007.md) | The events on the ITextInputPanel Interface that you can set attention for. |
| [enumALT_BREAKS enumeration](..\rectypes\ne-rectypes-enumalt_breaks.md) | Specifiers how to create alternates from a best result string. |
| [enumCONFIDENCE_LEVEL enumeration](..\rectypes\ne-rectypes-enumconfidence_level.md) | Indicates the level of confidence the recognizer has in the recognition result. |
| [enumLINE_METRICS enumeration](..\rectypes\ne-rectypes-enumline_metrics.md) | Represents the lines found in a recognition segment. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDynamicRenderer interface](..\rtscom\nn-rtscom-idynamicrenderer.md) | Displays the tablet pen data in real-time as that data is being handled by the RealTimeStylus Class object. |
| [IGestureRecognizer interface](..\rtscom\nn-rtscom-igesturerecognizer.md) | Reacts to events by recognizing gestures and adding gesture data to the input queue. |
| [IHandwrittenTextInsertion interface](..\peninputpanel\nn-peninputpanel-ihandwrittentextinsertion.md) | Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store. |
| [IInkCursor interface](..\msinkaut\nn-msinkaut-iinkcursor.md) | Represents general information about the tablet cursor. |
| [IInkCursorButton interface](..\msinkaut\nn-msinkaut-iinkcursorbutton.md) | Represents general information about a button on a tablet pointing and selecting device. |
| [IInkCursorButtons interface](..\msinkaut\nn-msinkaut-iinkcursorbuttons.md) | Represents a collection of IInkCursorButton objects for an IInkCursor interface. |
| [IInkCursors interface](..\msinkaut\nn-msinkaut-iinkcursors.md) | Represents a collection of IInkCursor objects. |
| [IInkCustomStrokes interface](..\msinkaut\nn-msinkaut-iinkcustomstrokes.md) | Contains a collection of user-defined InkStrokes collections. |
| [IInkDivisionResult interface](..\msinkaut15\nn-msinkaut15-iinkdivisionresult.md) | Represents the layout analysis of the collection of strokes contained by the InkDivider object. |
| [IInkDivisionUnit interface](..\msinkaut15\nn-msinkaut15-iinkdivisionunit.md) | Represents a single structural element within an IInkDivisionResult object. |
| [IInkDivisionUnits interface](..\msinkaut15\nn-msinkaut15-iinkdivisionunits.md) | Contains a collection of IInkDivisionUnit objects that are contained in an IInkDivisionResult object. |
| [IInkEdit interface](..\inked\nn-inked-iinkedit.md) | TBD. |
| [IInkExtendedProperties interface](..\msinkaut\nn-msinkaut-iinkextendedproperties.md) | Represents a collection of IInkExtendedProperty objects that contain application-defined data. |
| [IInkExtendedProperty interface](..\msinkaut\nn-msinkaut-iinkextendedproperty.md) | Represents the ability to add your own data to a variety of objects within the Tablet PC object model. |
| [IInkGesture interface](..\msinkaut\nn-msinkaut-iinkgesture.md) | Represents the ability to query particular properties of a gesture returned from a gesture recognition. |
| [IInkLineInfo interface](..\msinkaut\nn-msinkaut-iinklineinfo.md) | The IInkLineInfo interface provides access to the display properties and recognition result list of a text ink object (tInk). |
| [IInkRecognitionAlternate interface](..\msinkaut\nn-msinkaut-iinkrecognitionalternate.md) | Represents the possible word matches for segments of ink that are compared to a recognizers dictionary. |
| [IInkRecognitionAlternates interface](..\msinkaut\nn-msinkaut-iinkrecognitionalternates.md) | Contains the IInkRecognitionAlternate objects that represent possible word matches for segments of ink. |
| [IInkRecognitionResult interface](..\msinkaut\nn-msinkaut-iinkrecognitionresult.md) | Represents the result of the recognition. The results of recognizing handwritten ink are returned in an IInkRecognitionResult object. |
| [IInkRecognizer interface](..\msinkaut\nn-msinkaut-iinkrecognizer.md) | Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an InkRecognizerContext object, which is used to perform the actual handwriting recognition. |
| [IInkRecognizer2 interface](..\msinkaut\nn-msinkaut-iinkrecognizer2.md) | Adds members to the IInkWordList2 Interface. |
| [IInkRecognizerContext2 interface](..\msinkaut\nn-msinkaut-iinkrecognizercontext2.md) | Adds members to the InkRecognizerContext Class. |
| [IInkStrokeDisp interface](..\msinkaut\nn-msinkaut-iinkstrokedisp.md) | Represents a single ink stroke. |
| [IInkTablet interface](..\msinkaut\nn-msinkaut-iinktablet.md) | Represents the digitizer device of Tablet PC that receives tablet device messages or events. |
| [IInkTablet2 interface](..\msinkaut\nn-msinkaut-iinktablet2.md) | Extends the IInkTablet interface. |
| [IInkWordList2 interface](..\msinkaut\nn-msinkaut-iinkwordlist2.md) | Adds members to the InkWordList Class. |
| [IMathInputControl interface](..\micaut\nn-micaut-imathinputcontrol.md) | Exposes methods that turn ink input into interpreted math output. |
| [IRealTimeStylus interface](..\rtscom\nn-rtscom-irealtimestylus.md) | Handles the stylus packet data from a digitizer in real time. |
| [IRealTimeStylus2 interface](..\rtscom\nn-rtscom-irealtimestylus2.md) | Extends the IRealTimeStylus interface. |
| [IRealTimeStylus3 interface](..\rtscom\nn-rtscom-irealtimestylus3.md) | The IRealTimeStylus3 interface enables multitouch for the realtime stylus. |
| [IRealTimeStylusSynchronization interface](..\rtscom\nn-rtscom-irealtimestylussynchronization.md) | Synchronizes access to the RealTimeStylus Class object. |
| [IStrokeBuilder interface](..\rtscom\nn-rtscom-istrokebuilder.md) | Use interface to programmatically create strokes from packet data. |
| [IStylusAsyncPlugin interface](..\rtscom\nn-rtscom-istylusasyncplugin.md) | Represents an asynchronous plug-in that can be added to the asynchronous plug-in collection of the RealTimeStylus Class object. |
| [IStylusPlugin interface](..\rtscom\nn-rtscom-istylusplugin.md) | Receives notifications of RealTimeStylus Class events to enable you to perform custom processing based on those events. |
| [IStylusSyncPlugin interface](..\rtscom\nn-rtscom-istylussyncplugin.md) | Represents a synchronous plug-in that can be added to the RealTimeStylus Class object's synchronous plug-in collection. |
| [ITextInputPanel interface](..\peninputpanel\nn-peninputpanel-itextinputpanel.md) | Provides control of appearance and behavior of the Tablet PC Input Panel. |
| [ITextInputPanelEventSink interface](..\peninputpanel\nn-peninputpanel-itextinputpaneleventsink.md) | Defines methods that handle the ITextInputPanel Interface events. |
| [ITextInputPanelRunInfo interface](..\peninputpanel\nn-peninputpanel-itextinputpanelruninfo.md) | Provides a method to determine if the Text Input Panel is currently running. |
| [_IMathInputControlEvents interface](..\micaut\nn-micaut-_imathinputcontrolevents.md) | Exposes the math input control event handlers. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDynamicRenderer::Draw](..\rtscom\nf-rtscom-idynamicrenderer-draw.md) | Draws the cached data to the specified device context. |
| [IDynamicRenderer::Refresh](..\rtscom\nf-rtscom-idynamicrenderer-refresh.md) | Causes the DynamicRenderer Class object to redraw the ink data that is currently rendering. |
| [IDynamicRenderer::ReleaseCachedData](..\rtscom\nf-rtscom-idynamicrenderer-releasecacheddata.md) | Releases specified stroke data from the temporal data held by DynamicRenderer Class. |
| [IDynamicRenderer::get_ClipRectangle](..\rtscom\nf-rtscom-idynamicrenderer-get_cliprectangle.md) | Gets or sets the clipping rectangle for the DynamicRenderer Class object. |
| [IDynamicRenderer::get_ClipRegion](..\rtscom\nf-rtscom-idynamicrenderer-get_clipregion.md) | Gets or sets the clipping region for the DynamicRenderer Class object. |
| [IDynamicRenderer::get_DataCacheEnabled](..\rtscom\nf-rtscom-idynamicrenderer-get_datacacheenabled.md) | Gets or sets a value that indicates whether data caching is enabled for the DynamicRenderer Class object. |
| [IDynamicRenderer::get_DrawingAttributes](..\rtscom\nf-rtscom-idynamicrenderer-get_drawingattributes.md) | Gets or sets the DrawingAttributes object used by the DynamicRenderer Class object. |
| [IDynamicRenderer::get_Enabled](..\rtscom\nf-rtscom-idynamicrenderer-get_enabled.md) | Gets or sets a value that turns dynamic rendering on and off. |
| [IDynamicRenderer::get_HWND](..\rtscom\nf-rtscom-idynamicrenderer-get_hwnd.md) | Gets or sets the window handle, HWND, associated with the DynamicRenderer Class object. |
| [IDynamicRenderer::put_ClipRectangle](..\rtscom\nf-rtscom-idynamicrenderer-put_cliprectangle.md) | Gets or sets the clipping rectangle for the DynamicRenderer Class object. |
| [IDynamicRenderer::put_ClipRegion](..\rtscom\nf-rtscom-idynamicrenderer-put_clipregion.md) | Gets or sets the clipping region for the DynamicRenderer Class object. |
| [IDynamicRenderer::put_DataCacheEnabled](..\rtscom\nf-rtscom-idynamicrenderer-put_datacacheenabled.md) | Gets or sets a value that indicates whether data caching is enabled for the DynamicRenderer Class object. |
| [IDynamicRenderer::put_Enabled](..\rtscom\nf-rtscom-idynamicrenderer-put_enabled.md) | Gets or sets a value that turns dynamic rendering on and off. |
| [IDynamicRenderer::put_HWND](..\rtscom\nf-rtscom-idynamicrenderer-put_hwnd.md) | Gets or sets the window handle, HWND, associated with the DynamicRenderer Class object. |
| [IGestureRecognizer::EnableGestures](..\rtscom\nf-rtscom-igesturerecognizer-enablegestures.md) | Sets a value that indicates to which application gestures the GestureRecognizer Class object responds. |
| [IGestureRecognizer::Reset](..\rtscom\nf-rtscom-igesturerecognizer-reset.md) | Deletes past stroke information from the GestureRecognizer Class object. |
| [IGestureRecognizer::get_Enabled](..\rtscom\nf-rtscom-igesturerecognizer-get_enabled.md) | Gets or sets a value that indicates whether gesture recognition is enabled. |
| [IGestureRecognizer::get_MaxStrokeCount](..\rtscom\nf-rtscom-igesturerecognizer-get_maxstrokecount.md) | Gets or sets the maximum number of strokes allowed per gesture recognition. |
| [IGestureRecognizer::put_Enabled](..\rtscom\nf-rtscom-igesturerecognizer-put_enabled.md) | Gets or sets a value that indicates whether gesture recognition is enabled. |
| [IGestureRecognizer::put_MaxStrokeCount](..\rtscom\nf-rtscom-igesturerecognizer-put_maxstrokecount.md) | Gets or sets the maximum number of strokes allowed per gesture recognition. |
| [IHandwrittenTextInsertion::InsertInkRecognitionResult](..\peninputpanel\nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult.md) | Inserts recognition results. |
| [IHandwrittenTextInsertion::InsertRecognitionResultsArray](..\peninputpanel\nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray.md) | Insert recognition results array. |
| [IInkCollector::SetAllTabletsMode](..\msinkaut\nf-msinkaut-iinkcollector-setalltabletsmode.md) | Allows an ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from any tablet attached to the Tablet PC. |
| [IInkCollector::SetEventInterest](..\msinkaut\nf-msinkaut-iinkcollector-seteventinterest.md) | Modifies a value that indicates whether an object or control has interest in a specified event. |
| [IInkCollector::get_CollectingInk](..\msinkaut\nf-msinkaut-iinkcollector-get_collectingink.md) | Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture). |
| [IInkCollector::get_DefaultDrawingAttributes](..\msinkaut\nf-msinkaut-iinkcollector-get_defaultdrawingattributes.md) | Gets or sets the default drawing attributes to use when drawing and displaying ink. |
| [IInkCollector::get_Ink](..\msinkaut\nf-msinkaut-iinkcollector-get_ink.md) | Gets or sets the InkDisp object that is associated with an InkCollector object or an InkOverlay object. |
| [IInkCollector::put_CollectionMode](..\msinkaut\nf-msinkaut-iinkcollector-put_collectionmode.md) | Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes. |
| [IInkCollector::put_DynamicRendering](..\msinkaut\nf-msinkaut-iinkcollector-put_dynamicrendering.md) | Gets or sets the value that specifies whether ink is rendered as it is drawn. |
| [IInkCollector::put_Enabled](..\msinkaut\nf-msinkaut-iinkcollector-put_enabled.md) | Gets or sets a value that specifies whether the InkCollector object collects pen input (in-air packets, cursor in range events, and so on). |
| [IInkCollector::put_MousePointer](..\msinkaut\nf-msinkaut-iinkcollector-put_mousepointer.md) | Gets or sets a value that indicates the type of mouse pointer that appears. |
| [IInkCollector::put_hWnd](..\msinkaut\nf-msinkaut-iinkcollector-put_hwnd.md) | Gets or sets the handle value of the window on which ink is drawn. |
| [IInkCollector::putref_DefaultDrawingAttributes](..\msinkaut\nf-msinkaut-iinkcollector-putref_defaultdrawingattributes.md) | Gets or sets the default drawing attributes to use when drawing and displaying ink. |
| [IInkCursor::get_Buttons](..\msinkaut\nf-msinkaut-iinkcursor-get_buttons.md) | Gets the IInkCursorButtons collection that is available on an IInkCursor. |
| [IInkCursor::get_DrawingAttributes](..\msinkaut\nf-msinkaut-iinkcursor-get_drawingattributes.md) | Gets or sets the drawing attributes to apply to ink as it is drawn. |
| [IInkCursor::get_Id](..\msinkaut\nf-msinkaut-iinkcursor-get_id.md) | Gets the identifier of an object. |
| [IInkCursor::get_Inverted](..\msinkaut\nf-msinkaut-iinkcursor-get_inverted.md) | Gets a value that indicates whether the cursor is the inverted end of the pen. |
| [IInkCursor::get_Name](..\msinkaut\nf-msinkaut-iinkcursor-get_name.md) | Gets the name of the object. |
| [IInkCursor::get_Tablet](..\msinkaut\nf-msinkaut-iinkcursor-get_tablet.md) | Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input. |
| [IInkCursor::putref_DrawingAttributes](..\msinkaut\nf-msinkaut-iinkcursor-putref_drawingattributes.md) | Gets or sets the drawing attributes to apply to ink as it is drawn. |
| [IInkCursorButton::get_Id](..\msinkaut\nf-msinkaut-iinkcursorbutton-get_id.md) | Gets the identifier of an object. |
| [IInkCursorButton::get_Name](..\msinkaut\nf-msinkaut-iinkcursorbutton-get_name.md) | Gets the name of the object. |
| [IInkCursorButton::get_State](..\msinkaut\nf-msinkaut-iinkcursorbutton-get_state.md) | Gets the state of a cursor button, such as whether the button is unavailable, up, or down. |
| [IInkCursorButtons::Item](..\msinkaut\nf-msinkaut-iinkcursorbuttons-item.md) | Retrieves the IInkCursorButton object at the specified index or string identifier within the IInkCursorButtons collection. |
| [IInkCursorButtons::get_Count](..\msinkaut\nf-msinkaut-iinkcursorbuttons-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkCursors::Item](..\msinkaut\nf-msinkaut-iinkcursors-item.md) | Returns the IInkCursor object at the specified index within the IInkCursors collection. |
| [IInkCursors::get_Count](..\msinkaut\nf-msinkaut-iinkcursors-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkCustomStrokes::Add](..\msinkaut\nf-msinkaut-iinkcustomstrokes-add.md) | Adds an InkStrokes collection to an IInkCustomStrokes collection. |
| [IInkCustomStrokes::Clear](..\msinkaut\nf-msinkaut-iinkcustomstrokes-clear.md) | Clears all InkStrokes collections from the IInkCustomStrokes collection. |
| [IInkCustomStrokes::Item](..\msinkaut\nf-msinkaut-iinkcustomstrokes-item.md) | Retrieves the InkStrokes Collection at the location specified within the IInkCustomStrokes Interface. |
| [IInkCustomStrokes::get_Count](..\msinkaut\nf-msinkaut-iinkcustomstrokes-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkDivisionResult::ResultByType](..\msinkaut15\nf-msinkaut15-iinkdivisionresult-resultbytype.md) | Gets the requested structural units of the analysis results for an IInkDivisionUnits collection. |
| [IInkDivisionResult::get_Strokes](..\msinkaut15\nf-msinkaut15-iinkdivisionresult-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkDivisionUnit::get_DivisionType](..\msinkaut15\nf-msinkaut15-iinkdivisionunit-get_divisiontype.md) | Gets the type of structural unit the IInkDivisionUnit object represents within the analysis results. |
| [IInkDivisionUnit::get_RotationTransform](..\msinkaut15\nf-msinkaut15-iinkdivisionunit-get_rotationtransform.md) | Gets the transformation matrix that the IInkDivisionUnit object uses to rotate the strokes to horizontal. |
| [IInkDivisionUnit::get_Strokes](..\msinkaut15\nf-msinkaut15-iinkdivisionunit-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkDivisionUnits::Item](..\msinkaut15\nf-msinkaut15-iinkdivisionunits-item.md) | Retrieves the IInkDivisionUnit object at the specified index within the IInkDivisionUnits collection. |
| [IInkDivisionUnits::get_Count](..\msinkaut15\nf-msinkaut15-iinkdivisionunits-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkExtendedProperties::Add](..\msinkaut\nf-msinkaut-iinkextendedproperties-add.md) | Creates and adds an IInkExtendedProperty object to the IInkExtendedProperties collection. |
| [IInkExtendedProperties::Clear](..\msinkaut\nf-msinkaut-iinkextendedproperties-clear.md) | Clears all of the IInkExtendedProperty objects from the IInkExtendedProperties collection. |
| [IInkExtendedProperties::DoesPropertyExist](..\msinkaut\nf-msinkaut-iinkextendedproperties-doespropertyexist.md) | Retrieves a value that indicates whether an IInkExtendedProperty object exists within an IInkExtendedProperties collection. |
| [IInkExtendedProperties::Item](..\msinkaut\nf-msinkaut-iinkextendedproperties-item.md) | Retrieves the IInkExtendedProperty object at the specified index within the IInkExtendedProperties collection. |
| [IInkExtendedProperties::Remove](..\msinkaut\nf-msinkaut-iinkextendedproperties-remove.md) | Removes the IInkExtendedProperty object from the IInkExtendedProperties collection. |
| [IInkExtendedProperties::get_Count](..\msinkaut\nf-msinkaut-iinkextendedproperties-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkExtendedProperty::get_Data](..\msinkaut\nf-msinkaut-iinkextendedproperty-get_data.md) | Gets or sets the data of the extended property. |
| [IInkExtendedProperty::get_Guid](..\msinkaut\nf-msinkaut-iinkextendedproperty-get_guid.md) | Gets the globally unique identifier (GUID) of the IInkExtendedProperty object. |
| [IInkExtendedProperty::put_Data](..\msinkaut\nf-msinkaut-iinkextendedproperty-put_data.md) | Gets or sets the data of the extended property. |
| [IInkGesture::GetHotPoint](..\msinkaut\nf-msinkaut-iinkgesture-gethotpoint.md) | Gets the hot point of the gesture, in ink space coordinates. |
| [IInkGesture::get_Confidence](..\msinkaut\nf-msinkaut-iinkgesture-get_confidence.md) | Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an IInkRecognitionAlternate object or a gesture. |
| [IInkGesture::get_Id](..\msinkaut\nf-msinkaut-iinkgesture-get_id.md) | Gets the identifier of an object. |
| [IInkLineInfo::GetCandidate](..\msinkaut\nf-msinkaut-iinklineinfo-getcandidate.md) | Returns one recognition alternate from the recognition result list. |
| [IInkLineInfo::GetFormat](..\msinkaut\nf-msinkaut-iinklineinfo-getformat.md) | Returns the display properties currently set on the text ink object (tInk). |
| [IInkLineInfo::GetInkExtent](..\msinkaut\nf-msinkaut-iinklineinfo-getinkextent.md) | Specifies the display properties to set on the text ink object (tInk), and retrieves the width of the text ink object in HIMETRIC units. |
| [IInkLineInfo::Recognize](..\msinkaut\nf-msinkaut-iinklineinfo-recognize.md) | Reserved. |
| [IInkLineInfo::SetCandidate](..\msinkaut\nf-msinkaut-iinklineinfo-setcandidate.md) | Updates one recognition alternate in the recognition result list, either by replacing an existing alternate, or by adding an alternate to the list. |
| [IInkLineInfo::SetFormat](..\msinkaut\nf-msinkaut-iinklineinfo-setformat.md) | Specifies the display properties to set on the text ink object (tInk). |
| [IInkRecognitionAlternate::AlternatesWithConstantPropertyValues](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues.md) | Retrieves a IInkRecognitionAlternates collection, which are a division of the IInkRecognitionAlternate object on which this method is called. |
| [IInkRecognitionAlternate::GetPropertyValue](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-getpropertyvalue.md) | Retrieves the value of a specified property of the alternate. |
| [IInkRecognitionAlternate::GetStrokesFromStrokeRanges](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-getstrokesfromstrokeranges.md) | Retrieves the smallest InkStrokes collection that contains a known input InkStrokes collection and for which the IInkRecognizer object can provide alternates. |
| [IInkRecognitionAlternate::GetStrokesFromTextRange](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-getstrokesfromtextrange.md) | Retrives the collection that corresponds to the smallest set of recognition segments that contains a specified character range within the alternate. |
| [IInkRecognitionAlternate::GetTextRangeFromStrokes](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-gettextrangefromstrokes.md) | Retrieves the smallest range of recognized text for which the recognizer can return an alternate that contains a known InkStrokes collection. |
| [IInkRecognitionAlternate::get_Ascender](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_ascender.md) | Gets the ascender line for a IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_Baseline](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_baseline.md) | Gets the baseline for a IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_ConfidenceAlternates](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_confidencealternates.md) | Gets the collection of alternates in which each alternate in the collection consists of the segments with the same property values. |
| [IInkRecognitionAlternate::get_Confidence](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_confidence.md) | Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an IInkRecognitionAlternate object or a gesture. |
| [IInkRecognitionAlternate::get_Descender](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_descender.md) | Gets the decender line for an IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_LineAlternates](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_linealternates.md) | Gets the IInkRecognitionAlternates collection in which each alternate in the collection is on a separate line. |
| [IInkRecognitionAlternate::get_LineNumber](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_linenumber.md) | Gets the line number of the ink that makes up the alternate. |
| [IInkRecognitionAlternate::get_Midline](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_midline.md) | Gets the midline for a IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_String](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_string.md) | Gets the top string of the alternate. |
| [IInkRecognitionAlternate::get_Strokes](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkRecognitionAlternates::Item](..\msinkaut\nf-msinkaut-iinkrecognitionalternates-item.md) | Retrieves the IInkRecognitionAlternate object at the specified index within the IInkRecognitionAlternates collection. |
| [IInkRecognitionAlternates::get_Count](..\msinkaut\nf-msinkaut-iinkrecognitionalternates-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkRecognitionAlternates::get_Strokes](..\msinkaut\nf-msinkaut-iinkrecognitionalternates-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkRecognitionResult::ModifyTopAlternate](..\msinkaut\nf-msinkaut-iinkrecognitionresult-modifytopalternate.md) | Changes the top alternate of a recognition result by using the specified alternate. |
| [IInkRecognitionResult::SetResultOnStrokes](..\msinkaut\nf-msinkaut-iinkrecognitionresult-setresultonstrokes.md) | Assigns the recognition results to the strokes that were used to create the results. |
| [IInkRecognitionResult::get_Strokes](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkRecognitionResult::get_TopAlternate](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_topalternate.md) | Gets the top alternate of the recognition result. |
| [IInkRecognitionResult::get_TopConfidence](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_topconfidence.md) | Gets the top alternate of the recognition result. |
| [IInkRecognitionResult::get_TopString](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_topstring.md) | Gets the result text for the TopAlternate property. |
| [IInkRecognizer2::get_Id](..\msinkaut\nf-msinkaut-iinkrecognizer2-get_id.md) | Retrieves the ID for the InkRecognizer. |
| [IInkRecognizer2::get_UnicodeRanges](..\msinkaut\nf-msinkaut-iinkrecognizer2-get_unicoderanges.md) | Retrieves the Unicode ranges set for the current recognizer. |
| [IInkRecognizer::CreateRecognizerContext](..\msinkaut\nf-msinkaut-iinkrecognizer-createrecognizercontext.md) | Creates a new InkRecognizerContext object. |
| [IInkRecognizer::get_Capabilities](..\msinkaut\nf-msinkaut-iinkrecognizer-get_capabilities.md) | Gets the capabilities of the IInkRecognizer object. |
| [IInkRecognizer::get_Languages](..\msinkaut\nf-msinkaut-iinkrecognizer-get_languages.md) | Gets an array of language identifiers for the languages that the IInkRecognizer object supports. |
| [IInkRecognizer::get_Name](..\msinkaut\nf-msinkaut-iinkrecognizer-get_name.md) | Gets the name of the object. |
| [IInkRecognizer::get_PreferredPacketDescription](..\msinkaut\nf-msinkaut-iinkrecognizer-get_preferredpacketdescription.md) | Gets an array of globally unique identifiers (GUIDs) that represents the preferred packet properties for the recognizer. |
| [IInkRecognizer::get_SupportedProperties](..\msinkaut\nf-msinkaut-iinkrecognizer-get_supportedproperties.md) | Gets an array of globally unique identifiers (GUIDs) that describe the properties that the IInkRecognizer object supports. |
| [IInkRecognizer::get_Vendor](..\msinkaut\nf-msinkaut-iinkrecognizer-get_vendor.md) | Gets the vendor name of the IInkRecognizer object. |
| [IInkRecognizerContext2::get_EnabledUnicodeRanges](..\msinkaut\nf-msinkaut-iinkrecognizercontext2-get_enabledunicoderanges.md) | Gets or sets a set of one or more Unicode ranges that the recognizer context will support. |
| [IInkRecognizerContext2::put_EnabledUnicodeRanges](..\msinkaut\nf-msinkaut-iinkrecognizercontext2-put_enabledunicoderanges.md) | Gets or sets a set of one or more Unicode ranges that the recognizer context will support. |
| [IInkStrokeDisp::Clip](..\msinkaut\nf-msinkaut-iinkstrokedisp-clip.md) | Removes portions of an IInkStrokeDisp object or InkStrokes collection that are outside a rectangle. |
| [IInkStrokeDisp::FindIntersections](..\msinkaut\nf-msinkaut-iinkstrokedisp-findintersections.md) | Retrieves the points where this IInkStrokeDisp object intersects other IInkStrokeDisp objects within a known InkStrokes collection. |
| [IInkStrokeDisp::GetBoundingBox](..\msinkaut\nf-msinkaut-iinkstrokedisp-getboundingbox.md) | Retrieves the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or an InkStrokes collection. |
| [IInkStrokeDisp::GetFlattenedBezierPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-getflattenedbezierpoints.md) | Retrieves the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or a InkStrokes collection. |
| [IInkStrokeDisp::GetPacketData](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpacketdata.md) | Retrieves the packet data for a range of packets within the IInkStrokeDisp object. |
| [IInkStrokeDisp::GetPacketDescriptionPropertyMetrics](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics.md) | Retrieves the metrics for a given packet description type. |
| [IInkStrokeDisp::GetPacketValuesByProperty](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpacketvaluesbyproperty.md) | Retrieves the data for a known packet property from one or more packets in the stroke. |
| [IInkStrokeDisp::GetPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpoints.md) | Retrieves the points that make up a stroke. |
| [IInkStrokeDisp::GetRectangleIntersections](..\msinkaut\nf-msinkaut-iinkstrokedisp-getrectangleintersections.md) | Finds the points where a IInkStrokeDisp object intersects a given rectangle. |
| [IInkStrokeDisp::HitTestCircle](..\msinkaut\nf-msinkaut-iinkstrokedisp-hittestcircle.md) | Determines whether a stroke is either completely inside or intersected by a given circle. |
| [IInkStrokeDisp::Move](..\msinkaut\nf-msinkaut-iinkstrokedisp-move.md) | Applies a translation to the ink of an IInkStrokeDisp object or InkStrokes collection. |
| [IInkStrokeDisp::NearestPoint](..\msinkaut\nf-msinkaut-iinkstrokedisp-nearestpoint.md) | Finds the location on the stroke nearest to a known point and returns the distance that point is from the stroke. Everything is in ink space coordinates. |
| [IInkStrokeDisp::Rotate](..\msinkaut\nf-msinkaut-iinkstrokedisp-rotate.md) | Rotates the ink using an angle in degrees around a center point of the rotation. |
| [IInkStrokeDisp::ScaleToRectangle](..\msinkaut\nf-msinkaut-iinkstrokedisp-scaletorectangle.md) | Scales the IInkStrokeDisp object or InkStrokes collection to fit in the specified InkRectangle object. |
| [IInkStrokeDisp::ScaleTransform](..\msinkaut\nf-msinkaut-iinkstrokedisp-scaletransform.md) | Applies the specified horizontal and vertical factors to the transform or ink. |
| [IInkStrokeDisp::SetPacketValuesByProperty](..\msinkaut\nf-msinkaut-iinkstrokedisp-setpacketvaluesbyproperty.md) | Modifies the packet values for a particular property. |
| [IInkStrokeDisp::SetPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-setpoints.md) | Sets the points of the IInkStrokeDisp using an array of X, Y values. |
| [IInkStrokeDisp::Shear](..\msinkaut\nf-msinkaut-iinkstrokedisp-shear.md) | Shears the ink in the stroke or strokes by the specified horizontal and vertical factors. |
| [IInkStrokeDisp::Split](..\msinkaut\nf-msinkaut-iinkstrokedisp-split.md) | Splits the stroke at the specified location on the stroke. |
| [IInkStrokeDisp::Transform](..\msinkaut\nf-msinkaut-iinkstrokedisp-transform.md) | Applies a linear transformation to an IInkStrokeDisp object or an InkStrokes collection, which can represent scaling, rotation, translation, and combinations of transformations. |
| [IInkStrokeDisp::get_BezierCusps](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_beziercusps.md) | Gets an array that contains the indices of the cusps of the Bezier approximation of the stroke. |
| [IInkStrokeDisp::get_BezierPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_bezierpoints.md) | Gets the array of control points that represent the Bezier approximation of the stroke. |
| [IInkStrokeDisp::get_Deleted](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_deleted.md) | Gets a value that specifies whether a known stroke is deleted from the ink. |
| [IInkStrokeDisp::get_DrawingAttributes](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_drawingattributes.md) | Gets or sets the drawing attributes to apply to ink as it is drawn. |
| [IInkStrokeDisp::get_ID](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_id.md) | Gets the identifier of an object. |
| [IInkStrokeDisp::get_Ink](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_ink.md) | Gets the parent InkDisp object of a stroke. |
| [IInkStrokeDisp::get_PacketCount](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_packetcount.md) | Gets the number of packets received for an IInkStrokeDisp object. |
| [IInkStrokeDisp::get_PacketDescription](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_packetdescription.md) | Gets an array of globally unique identifiers (GUIDs) that describes the types of packet data stored in the IInkStrokeDisp object. |
| [IInkStrokeDisp::get_PacketSize](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_packetsize.md) | Gets the size, in bytes, of a packet. |
| [IInkStrokeDisp::get_PolylineCusps](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_polylinecusps.md) | Gets an array that contains the indices of the cusps of the IInkStrokeDisp object. |
| [IInkStrokeDisp::get_SelfIntersections](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_selfintersections.md) | Gets the self-intersections of the stroke. |
| [IInkTablet2::get_DeviceKind](..\msinkaut\nf-msinkaut-iinktablet2-get_devicekind.md) | Gets the type of Tablet device being used. |
| [IInkTablet3::get_IsMultiTouch](..\msinkaut\nf-msinkaut-iinktablet3-get_ismultitouch.md) | Gets a value that indicates whether an input device supports multitouch. |
| [IInkTablet3::get_MaximumCursors](..\msinkaut\nf-msinkaut-iinktablet3-get_maximumcursors.md) | Gets the maximum number of cursors that a tablet device supports. |
| [IInkTablet::GetPropertyMetrics](..\msinkaut\nf-msinkaut-iinktablet-getpropertymetrics.md) | Retrieves the metrics data for a specified property. |
| [IInkTablet::IsPacketPropertySupported](..\msinkaut\nf-msinkaut-iinktablet-ispacketpropertysupported.md) | Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported. |
| [IInkTablet::get_HardwareCapabilities](..\msinkaut\nf-msinkaut-iinktablet-get_hardwarecapabilities.md) | Gets a bitmask that defines the hardware capabilities of the tablet, such as whether a cursor must be in physical contact with the tablet to report its position. |
| [IInkTablet::get_MaximumInputRectangle](..\msinkaut\nf-msinkaut-iinktablet-get_maximuminputrectangle.md) | Gets the maximum input rectangle, in tablet device coordinates that the IInkTablet object supports. |
| [IInkTablet::get_Name](..\msinkaut\nf-msinkaut-iinktablet-get_name.md) | Gets the name of the object. |
| [IInkTablet::get_PlugAndPlayId](..\msinkaut\nf-msinkaut-iinktablet-get_plugandplayid.md) | Gets a string representation of the Plug and Play identifier of the IInkTablet object. |
| [IInkWordList2::AddWords](..\msinkaut\nf-msinkaut-iinkwordlist2-addwords.md) | Adds more than one word to an InkWordList in a single operation. |
| [IMathInputControl::AddFunctionName](..\micaut\nf-micaut-imathinputcontrol-addfunctionname.md) | Adds a new function-name definition to the list of custom math functions that the recognizer accepts. |
| [IMathInputControl::Clear](..\micaut\nf-micaut-imathinputcontrol-clear.md) | Clears all ink from the control. |
| [IMathInputControl::EnableAutoGrow](..\micaut\nf-micaut-imathinputcontrol-enableautogrow.md) | Determines whether the control automatically grows when input is entered beyond the control's current range. |
| [IMathInputControl::EnableExtendedButtons](..\micaut\nf-micaut-imathinputcontrol-enableextendedbuttons.md) | Determines whether the extended set of control buttons is shown. |
| [IMathInputControl::GetHoverIcon](..\micaut\nf-micaut-imathinputcontrol-gethovericon.md) | Retrieves the icon to be used for the hover target to launch math input control. |
| [IMathInputControl::GetPosition](..\micaut\nf-micaut-imathinputcontrol-getposition.md) | Retrieves the position and size of the control. |
| [IMathInputControl::GetPreviewHeight](..\micaut\nf-micaut-imathinputcontrol-getpreviewheight.md) | Retrieves the height in pixels of the preview area. |
| [IMathInputControl::Hide](..\micaut\nf-micaut-imathinputcontrol-hide.md) | Hides the control. |
| [IMathInputControl::IsVisible](..\micaut\nf-micaut-imathinputcontrol-isvisible.md) | Determines whether the control is visible. |
| [IMathInputControl::LoadInk](..\micaut\nf-micaut-imathinputcontrol-loadink.md) | Processes ink and triggers recognition. |
| [IMathInputControl::RemoveFunctionName](..\micaut\nf-micaut-imathinputcontrol-removefunctionname.md) | Removes a function-name definition from the list of custom math functions that the recognizer accepts. |
| [IMathInputControl::SetCaptionText](..\micaut\nf-micaut-imathinputcontrol-setcaptiontext.md) | Modifies the string that will be used as the control's caption when the window is created. |
| [IMathInputControl::SetCustomPaint](..\micaut\nf-micaut-imathinputcontrol-setcustompaint.md) | Determines whether a button or background has custom painting. |
| [IMathInputControl::SetOwnerWindow](..\micaut\nf-micaut-imathinputcontrol-setownerwindow.md) | Modifies the window that owns this control. |
| [IMathInputControl::SetPosition](..\micaut\nf-micaut-imathinputcontrol-setposition.md) | Modifies the location and size of the control. |
| [IMathInputControl::SetPreviewHeight](..\micaut\nf-micaut-imathinputcontrol-setpreviewheight.md) | Modifies the preview-area height in pixels. |
| [IMathInputControl::Show](..\micaut\nf-micaut-imathinputcontrol-show.md) | Shows the control. |
| [IRealTimeStylus2::get_FlicksEnabled](..\rtscom\nf-rtscom-irealtimestylus2-get_flicksenabled.md) | Returns a value indicating whether flick gestures are enabled for the RTS. |
| [IRealTimeStylus2::put_FlicksEnabled](..\rtscom\nf-rtscom-irealtimestylus2-put_flicksenabled.md) | Indicates if flick gesture recognition is enabled. |
| [IRealTimeStylus3::get_MultiTouchEnabled](..\rtscom\nf-rtscom-irealtimestylus3-get_multitouchenabled.md) | Indicates whether the IRealTimeStylus3 object has multitouch input enabled. |
| [IRealTimeStylus3::put_MultiTouchEnabled](..\rtscom\nf-rtscom-irealtimestylus3-put_multitouchenabled.md) | Indicates whether the IRealTimeStylus3 object has multitouch input enabled. |
| [IRealTimeStylus::AddCustomStylusDataToQueue](..\rtscom\nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue.md) | Adds custom data to the specified queue of the RealTimeStylus Class object. |
| [IRealTimeStylus::AddStylusAsyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-addstylusasyncplugin.md) | Adds an IStylusAsyncPlugin to the asynchronous plug-in collection at the specified index. |
| [IRealTimeStylus::AddStylusSyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-addstylussyncplugin.md) | Adds an IStylusSyncPlugin to the synchronous plug-in collection at the specified index. |
| [IRealTimeStylus::ClearStylusQueues](..\rtscom\nf-rtscom-irealtimestylus-clearstylusqueues.md) | Clears the RealTimeStylus Class input and output queues of data. |
| [IRealTimeStylus::GetAllTabletContextIds](..\rtscom\nf-rtscom-irealtimestylus-getalltabletcontextids.md) | Retrieves an array containing all of the currently active tablet context identifiers. |
| [IRealTimeStylus::GetDesiredPacketDescription](..\rtscom\nf-rtscom-irealtimestylus-getdesiredpacketdescription.md) | Retrieves the list of properties that have been requested to be included in the packet stream. |
| [IRealTimeStylus::GetPacketDescriptionData](..\rtscom\nf-rtscom-irealtimestylus-getpacketdescriptiondata.md) | Retrieves the packet properties and scaling factors. |
| [IRealTimeStylus::GetStylusAsyncPluginCount](..\rtscom\nf-rtscom-irealtimestylus-getstylusasyncplugincount.md) | Retrieves the number of plug-ins in the asynchronous plug-in collection. |
| [IRealTimeStylus::GetStylusAsyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-getstylusasyncplugin.md) | Retrieves the plug-in at the specified index in the asynchronous plug-in collection. |
| [IRealTimeStylus::GetStylusForId](..\rtscom\nf-rtscom-irealtimestylus-getstylusforid.md) | Retrieves a stylus for the specified stylus identifier. |
| [IRealTimeStylus::GetStylusSyncPluginCount](..\rtscom\nf-rtscom-irealtimestylus-getstylussyncplugincount.md) | Retrieves the number of plug-ins in the synchronous plug-in collection. |
| [IRealTimeStylus::GetStylusSyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-getstylussyncplugin.md) | Retrieves the plug-in at the specified index in the synchronous plug-in collection. |
| [IRealTimeStylus::GetStyluses](..\rtscom\nf-rtscom-irealtimestylus-getstyluses.md) | Retrieves the collection of styluses the RealTimeStylus Class object has encountered. |
| [IRealTimeStylus::GetTabletContextIdFromTablet](..\rtscom\nf-rtscom-irealtimestylus-gettabletcontextidfromtablet.md) | Retrieves the TabletContextId property that is associated with a given tablet digitizer object. |
| [IRealTimeStylus::GetTabletFromTabletContextId](..\rtscom\nf-rtscom-irealtimestylus-gettabletfromtabletcontextid.md) | Retrieves an IInkTablet Interface for a specified tablet context. |
| [IRealTimeStylus::GetTablet](..\rtscom\nf-rtscom-irealtimestylus-gettablet.md) | Retrieves an IInkTablet Interface object to the caller. |
| [IRealTimeStylus::RemoveAllStylusAsyncPlugins](..\rtscom\nf-rtscom-irealtimestylus-removeallstylusasyncplugins.md) | Removes all the plug-ins from the asynchronous plug-in collection. |
| [IRealTimeStylus::RemoveAllStylusSyncPlugins](..\rtscom\nf-rtscom-irealtimestylus-removeallstylussyncplugins.md) | Removes all of the plug-ins from the synchronous plug-in collection. |
| [IRealTimeStylus::RemoveStylusAsyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-removestylusasyncplugin.md) | Removes and optionally returns an IStylusAsyncPlugin with the specified index in the asynchronous plug-in collection. |
| [IRealTimeStylus::RemoveStylusSyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-removestylussyncplugin.md) | Removes an IStylusSyncPlugin from the collection at the specified index. |
| [IRealTimeStylus::SetAllTabletsMode](..\rtscom\nf-rtscom-irealtimestylus-setalltabletsmode.md) | Sets the mode for the RealTimeStylus Class object to collect data from all digitizers. |
| [IRealTimeStylus::SetDesiredPacketDescription](..\rtscom\nf-rtscom-irealtimestylus-setdesiredpacketdescription.md) | Requests properties to be included in the packet stream. |
| [IRealTimeStylus::SetSingleTabletMode](..\rtscom\nf-rtscom-irealtimestylus-setsingletabletmode.md) | Modifies the mode for RealTimeStylus Class (RTS) object to collect input from only one tablet object representing a digitizer attached to the Tablet PC. Stylus input from other digitizers is ignored by the RealTimeStylus. |
| [IRealTimeStylus::get_ChildRealTimeStylusPlugin](..\rtscom\nf-rtscom-irealtimestylus-get_childrealtimestylusplugin.md) | Gets or sets a RealTimeStylus object as an asynchronous plug-in of the current RealTimeStylus object. |
| [IRealTimeStylus::get_Enabled](..\rtscom\nf-rtscom-irealtimestylus-get_enabled.md) | Gets or sets a value that specifies whether the RealTimeStylus object collects tablet pen data. |
| [IRealTimeStylus::get_HWND](..\rtscom\nf-rtscom-irealtimestylus-get_hwnd.md) | Gets or sets the handle value associated with the window the RealTimeStylus object uses. |
| [IRealTimeStylus::get_WindowInputRectangle](..\rtscom\nf-rtscom-irealtimestylus-get_windowinputrectangle.md) | Gets or sets the window input rectangle for the RealTimeStylus Class object. |
| [IRealTimeStylus::put_Enabled](..\rtscom\nf-rtscom-irealtimestylus-put_enabled.md) | Gets or sets a value that specifies whether the RealTimeStylus object collects tablet pen data. |
| [IRealTimeStylus::put_HWND](..\rtscom\nf-rtscom-irealtimestylus-put_hwnd.md) | Gets or sets the handle value associated with the window the RealTimeStylus object uses. |
| [IRealTimeStylus::put_WindowInputRectangle](..\rtscom\nf-rtscom-irealtimestylus-put_windowinputrectangle.md) | Gets or sets the window input rectangle for the RealTimeStylus Class object. |
| [IRealTimeStylusSynchronization::AcquireLock](..\rtscom\nf-rtscom-irealtimestylussynchronization-acquirelock.md) | Retrieves the specified lock. |
| [IRealTimeStylusSynchronization::ReleaseLock](..\rtscom\nf-rtscom-irealtimestylussynchronization-releaselock.md) | Releases the specified lock. |
| [IStrokeBuilder::AppendPackets](..\rtscom\nf-rtscom-istrokebuilder-appendpackets.md) | Adds a packet to the end of the digitizer input packet list. |
| [IStrokeBuilder::BeginStroke](..\rtscom\nf-rtscom-istrokebuilder-beginstroke.md) | Begins a stroke on an ink object by using packet data from a RealTimeStylus Class object. |
| [IStrokeBuilder::CreateStroke](..\rtscom\nf-rtscom-istrokebuilder-createstroke.md) | Creates strokes on an ink object by using packet data that came from a RealTimeStylus Class object. |
| [IStrokeBuilder::EndStroke](..\rtscom\nf-rtscom-istrokebuilder-endstroke.md) | Ends a stroke and returns the stroke object. |
| [IStrokeBuilder::get_Ink](..\rtscom\nf-rtscom-istrokebuilder-get_ink.md) | Gets or sets the ink object that is associated with the IStrokeBuilder object. |
| [IStylusPlugin::CustomStylusDataAdded](..\rtscom\nf-rtscom-istylusplugin-customstylusdataadded.md) | Notifies the implementing plug-in that custom stylus data is available. |
| [IStylusPlugin::DataInterest](..\rtscom\nf-rtscom-istylusplugin-datainterest.md) | Retrieves the events for which the plug-in is to receive notifications. |
| [IStylusPlugin::Error](..\rtscom\nf-rtscom-istylusplugin-error.md) | Notifies the implementing object that this plug-in or one of the previous plug-ins in either the IStylusAsyncPlugin or IStylusSyncPlugin collection threw an exception. |
| [IStylusPlugin::InAirPackets](..\rtscom\nf-rtscom-istylusplugin-inairpackets.md) | Notifies the object implementing the plug-in that the stylus is moving above the digitizer. |
| [IStylusPlugin::Packets](..\rtscom\nf-rtscom-istylusplugin-packets.md) | Notifies the object implementing the plug-in that the tablet pen is moving on the digitizer. |
| [IStylusPlugin::RealTimeStylusDisabled](..\rtscom\nf-rtscom-istylusplugin-realtimestylusdisabled.md) | Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is disabled. |
| [IStylusPlugin::RealTimeStylusEnabled](..\rtscom\nf-rtscom-istylusplugin-realtimestylusenabled.md) | Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is enabled. |
| [IStylusPlugin::StylusButtonDown](..\rtscom\nf-rtscom-istylusplugin-stylusbuttondown.md) | Notifies the implementing plug-in that the user is pressing a stylus button. |
| [IStylusPlugin::StylusButtonUp](..\rtscom\nf-rtscom-istylusplugin-stylusbuttonup.md) | Notifies the implementing plug-in that the user has released a stylus button. |
| [IStylusPlugin::StylusDown](..\rtscom\nf-rtscom-istylusplugin-stylusdown.md) | Notifies the implementing plug-in that the tablet pen has touched the digitizer surface. |
| [IStylusPlugin::StylusInRange](..\rtscom\nf-rtscom-istylusplugin-stylusinrange.md) | Notifies the implementing plug-in that the stylus is entering the detection range of the digitizer. |
| [IStylusPlugin::StylusOutOfRange](..\rtscom\nf-rtscom-istylusplugin-stylusoutofrange.md) | Notifies the implementing plug-in that the stylus has left the detection range of the digitizer. |
| [IStylusPlugin::StylusUp](..\rtscom\nf-rtscom-istylusplugin-stylusup.md) | Notifies the implementing plug-in that the user has raised the tablet pen from the tablet digitizer surface. |
| [IStylusPlugin::SystemEvent](..\rtscom\nf-rtscom-istylusplugin-systemevent.md) | Notifies the implementing plug-in that a system event is available. |
| [IStylusPlugin::TabletAdded](..\rtscom\nf-rtscom-istylusplugin-tabletadded.md) | Notifies an implementing plug-in when an ITablet object is attached to the system. |
| [IStylusPlugin::TabletRemoved](..\rtscom\nf-rtscom-istylusplugin-tabletremoved.md) | Notifies an implementing plug-in when an ITablet object is removed from the system. |
| [IStylusPlugin::UpdateMapping](..\rtscom\nf-rtscom-istylusplugin-updatemapping.md) | Notifies the plug-in when display properties, such as dpi or orientation, change. |
| [ITextInputPanel::Advise](..\peninputpanel\nf-peninputpanel-itextinputpanel-advise.md) | Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object. |
| [ITextInputPanel::CommitPendingInput](..\peninputpanel\nf-peninputpanel-itextinputpanel-commitpendinginput.md) | Sends collected ink to the recognizer and posts the recognition result. |
| [ITextInputPanel::SetInPlaceHoverTargetPosition](..\peninputpanel\nf-peninputpanel-itextinputpanel-setinplacehovertargetposition.md) | Explicitly positions the Tablet PC Input Panel hover target in screen coordinates. |
| [ITextInputPanel::SetInPlacePosition](..\peninputpanel\nf-peninputpanel-itextinputpanel-setinplaceposition.md) | Explicitly positions the Tablet PC Input Panel in screen coordinates. |
| [ITextInputPanel::SetInPlaceVisibility](..\peninputpanel\nf-peninputpanel-itextinputpanel-setinplacevisibility.md) | Shows or hides the Tablet PC Input Panel. |
| [ITextInputPanel::Unadvise](..\peninputpanel\nf-peninputpanel-itextinputpanel-unadvise.md) | Terminates an advisory connection previously established through ITextInputPanel |
| [ITextInputPanel::get_AttachedEditWindow](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_attachededitwindow.md) | Gets or sets the window handle of the object to which the ITextInputPanel object is attached. |
| [ITextInputPanel::get_CurrentCorrectionMode](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentcorrectionmode.md) | Gets the current correction comb mode as specified by the CorrectionMode Enumeration. |
| [ITextInputPanel::get_CurrentInPlaceState](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentinplacestate.md) | Gets the current in-place state as specified by the InPlaceState Enumeration. |
| [ITextInputPanel::get_CurrentInputArea](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentinputarea.md) | Gets the current input area as specified by the PanelInputArea Enumeration. |
| [ITextInputPanel::get_CurrentInteractionMode](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentinteractionmode.md) | Gets the positioning of the Tablet PC Input Panel as specified by the InteractionMode Enumeration. |
| [ITextInputPanel::get_DefaultInPlaceState](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_defaultinplacestate.md) | Gets or sets the default in-place state as specified by the InPlaceState Enumeration. |
| [ITextInputPanel::get_DefaultInputArea](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_defaultinputarea.md) | Gets or sets the default input area as specified by the PanelInputArea Enumeration. |
| [ITextInputPanel::get_ExpandPostInsertionCorrection](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_expandpostinsertioncorrection.md) | Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded. |
| [ITextInputPanel::get_InPlaceBoundingRectangle](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle.md) | Gets the bounding rectangle for Tablet PC Input Panel. |
| [ITextInputPanel::get_InPlaceVisibleOnFocus](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_inplacevisibleonfocus.md) | Gets or sets a value that indicates whether the Tablet PC Input Panel is displayed automatically when the window to which it is attached gets focus. |
| [ITextInputPanel::get_PopDownCorrectionHeight](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_popdowncorrectionheight.md) | Gets the height of the Post-Insertion correction comb when it is positioned below Input Panel. |
| [ITextInputPanel::get_PopUpCorrectionHeight](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_popupcorrectionheight.md) | Gets the height of the Post-Insertion correction comb when it is positioned above Input Panel. |
| [ITextInputPanel::get_PreferredInPlaceDirection](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_preferredinplacedirection.md) | Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field. |
| [ITextInputPanel::put_AttachedEditWindow](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_attachededitwindow.md) | Gets or sets the window handle of the object to which the ITextInputPanel object is attached. |
| [ITextInputPanel::put_DefaultInPlaceState](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_defaultinplacestate.md) | Gets or sets the default in-place state as specified by the InPlaceState Enumeration. |
| [ITextInputPanel::put_DefaultInputArea](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_defaultinputarea.md) | Gets or sets the default input area as specified by the PanelInputArea Enumeration. |
| [ITextInputPanel::put_ExpandPostInsertionCorrection](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_expandpostinsertioncorrection.md) | Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded. |
| [ITextInputPanel::put_InPlaceVisibleOnFocus](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_inplacevisibleonfocus.md) | Gets or sets a value that indicates whether the Tablet PC Input Panel is displayed automatically when the window to which it is attached gets focus. |
| [ITextInputPanel::put_PreferredInPlaceDirection](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_preferredinplacedirection.md) | Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field. |
| [ITextInputPanelEventSink::CorrectionModeChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-correctionmodechanged.md) | Occurs when the correction comb on the Tablet PC Input Panel has changed modes. |
| [ITextInputPanelEventSink::CorrectionModeChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-correctionmodechanging.md) | Occurs when the correction comb on the Tablet PC Input Panel is about to change modes. |
| [ITextInputPanelEventSink::InPlaceSizeChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacesizechanged.md) | Occurs when the in-place Input Panel size has changed due to a user resize, auto growth, or an input area change. |
| [ITextInputPanelEventSink::InPlaceSizeChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging.md) | Occurs when the in-place Input Panel size is about to change due to a user resize, auto growth, or an input area change. |
| [ITextInputPanelEventSink::InPlaceStateChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacestatechanged.md) | Occurs when the In-Place state has changed. |
| [ITextInputPanelEventSink::InPlaceStateChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacestatechanging.md) | Occurs when the In-Place state is about to change. |
| [ITextInputPanelEventSink::InPlaceVisibilityChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanged.md) | Occurs when the Tablet PC Input Panel has switched between visible and invisible. |
| [ITextInputPanelEventSink::InPlaceVisibilityChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanging.md) | Occurs when the Tablet PC Input Panel is about to switch between visible and invisible. |
| [ITextInputPanelEventSink::InputAreaChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inputareachanged.md) | Occurs when the input area has changed on the Tablet PC Input Panel. |
| [ITextInputPanelEventSink::InputAreaChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inputareachanging.md) | Occurs when the input area is about to change on the Tablet PC Input Panel. |
| [ITextInputPanelEventSink::TextInserted](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-textinserted.md) | Occurs when the Tablet PC Input Panel has inserted text into the control with input focus. Provides access to the ink the user entered in the Input Panel. |
| [ITextInputPanelEventSink::TextInserting](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-textinserting.md) | Occurs when the Tablet PC Input Panel is about to insert text into the control with input focus. Provides access to the ink the user entered in the Input Panel. |
| [ITextInputPanelRunInfo::IsTipRunning](..\peninputpanel\nf-peninputpanel-itextinputpanelruninfo-istiprunning.md) | Indicates if the Tablet PC Input Panel is running at the time the method is called. |
